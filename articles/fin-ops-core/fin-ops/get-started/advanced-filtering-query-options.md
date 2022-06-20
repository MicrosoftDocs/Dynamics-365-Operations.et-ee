---
title: Täpsem filtreerimine ja päringusüntaks
description: See artikkel kirjeldab filtreerimise ja päringu suvandeid täpsema filtri/sortimise dialoogi jaoks ja vastete tehtemärki filtripaanil või võrgustiku veeru päise filtrites.
author: jasongre
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
ms.openlocfilehash: 520c8b32099024e9a9619a6ecdcd3ba7b97c7ecf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856914"
---
# <a name="advanced-filtering-and-query-syntax"></a>Täpsema filtreerimise ja päringu süntaks

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

See artikkel kirjeldab filtreerimis- ja päringuvalikuid, mis on saadaval, kui kasutate filtripaanil või ruudustiku veerupäisefiltrites dialoogi Täpsem filter / sortimine või tehtemärki **vastab**.

## <a name="advanced-query-syntax"></a>Täpsem päringusüntaks

<table>
<thead>
<tr>
<th>Süntaks</th>
<th>Märgi kirjeldus</th>
<th>Kirjeldus</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>väärtus</em></td>
<td>Võrdub sisestatud väärtusega</td>
<td>Tippige väärtus, mille soovite leida.</td>
<td><strong>Sepp</strong> leiab väärtuse &quot;Sepp&quot;.</td>
</tr>
<tr>
<td>!<em>väärtus</em> (hüüumärk)</td>
<td>Ei võrdu sisestatud väärtusega</td>
<td>Tippige hüüumärk ja seejärel väärtus, mille soovite välistada.</td>
<td><strong>!Sepp</strong> leiab kõik väärtused, välja arvatud &quot;Sepp&quot;.</td>
</tr>
<tr>
<td><em>algväärtus</em>..<em>lõppväärtus</em> (topeltpunkt)</td>
<td>Kahe teineteisest topeltpunktiga eraldatud sisestatud väärtuse vahel</td>
<td>Tippige algväärtus, seejärel kaks punkti ja siis lõppväärtus.</td>
<td><strong>1..10</strong> leiab kõik väärtused vahemikus 1 kuni 10. Kuid näiteks stringiväljal leiab <strong>A..C</strong> kõik tähtedega &quot;A&quot; ja &quot;B&quot; algavad väärtused ning väärtused, mis võrduvad täpselt tähega &quot;C&quot;. Näiteks ei leia see päring stringi &quot;Ca&quot;. Selleks et leida kõiki väärtusi vahemikus &quot;A<em>&quot; kuni &quot;C</em>&quot;, tippige <strong>A..D</strong>.</td>
</tr>
<tr>
<td>..<em>väärtus</em> (topeltpunkt)</td>
<td>Sisestatud väärtusest väiksem või sellega võrdne</td>
<td>Tippige kaks punkti ja seejärel väärtus.</td>
<td><strong>..1000</strong> leiab iga tuhandest väiksema või sellega võrdse arvu, näiteks &quot;100&quot;, &quot;999,95&quot; ja &quot;1000&quot;.</td>
</tr>
<tr>
<td><em>väärtus</em>.. (topeltpunkt)</td>
<td>Sisestatud väärtusest suurem või sellega võrdne</td>
<td>Tippige väärtus ja seejärel kaks punkti.</td>
<td><strong>1000..</strong> leiab iga tuhandest suurema või sellega võrdse arvu, näiteks &quot;1000&quot;, &quot;1000,01&quot; ja &quot;1 000 000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>väärtus</em> (märk „suurem kui”)</td>
<td>Sisestatud väärtusest suurem</td>
<td>Tippige märk „suurem kui” (<strong>&gt;</strong>) ja seejärel väärtus.</td>
<td><strong>&gt;1000</strong> leiab iga tuhandest suurema arvu, näiteks &quot;1000,01&quot;, &quot;20 000&quot; ja &quot;1 000 000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>väärtus</em> (märk „väiksem kui”)</td>
<td>Sisestatud väärtusest väiksem</td>
<td>Tippige märk „väiksem kui” (<strong>&lt;</strong>) ja seejärel väärtus.</td>
<td><strong>&lt;1000</strong> leiab iga tuhandest väiksema arvu, näiteks &quot;999,99&quot;, &quot;1&quot; ja &quot;–200&quot;.</td>
</tr>
<tr>
<td><em>väärtus</em>* (tärn)</td>
<td>Sisestatud väärtusega algav</td>
<td>Tippige lähteväärtus ja selle järele tärn (<strong>*</strong>).</td>
<td><strong>S*</strong> leiab iga S-tähega algava stringi, näiteks &quot;S&quot;, nagu &quot;Stockholm&quot;, &quot;Sindi&quot; ja &quot;San Francisco&quot;.</td>
</tr>
<tr>
<td>*<em>väärtus</em> (tärn)</td>
<td>Sisestatud väärtusega lõppev</td>
<td>Tippige tärn ja selle järele lõppväärtus.</td>
<td><strong>*vere</strong> leiab iga &quot;vere&quot;-lõpulise stringi, näiteks &quot;Adavere&quot; ja &quot;Pandivere&quot;.</td>
</tr>
<tr>
<td>*<em>väärtus</em>* (tärn)</td>
<td>Sisaldab sisestatud väärtust</td>
<td>Tippige tärn, otsitav väärtus ja selle järele veel üks tärn.</td>
<td><strong>*rn*</strong> leiab iga stringi, milles sisaldub täheühend &quot;rn&quot;, näiteks &quot;Pärnu&quot; ja &quot;Kernu&quot;.</td>
</tr>
<tr>
<td>? (küsimärk)</td>
<td>Ühte või mitut tundmatut märki sisaldav</td>
<td>Tippige väärtuses tundmatu märgi asemele küsimärk.</td>
<td><strong>Ma?i</strong> leiab nii &quot;Mari&quot; kui ka &quot;Mati&quot;.</td>
</tr>
<tr>
<td><em>väärtus</em>,<em>väärtus</em> (koma)</td>
<td>Vastendab sobivad väärtused komadega eraldatult</td>
<td>Tippige kõik kriteeriumid, eraldades need komadega.</td>
<td><strong>A, D, F, G</strong> leiab täpselt &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ja &quot;G&quot;. <strong>10, 20, 30, 100</strong> leiab täpselt &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr>
<td>"" (kaks kahekordset jutumärki)</td>
<td>Tühja väärtuse sobitamine</td>
<td>Tippige kaks järjestikust kahekordset jutumärki, et filtreerida selle välja tühjad väärtused.</td>
<td>Kaks järjestikust kahekordset jutumärki (<strong>"</strong>") leiab ilma väärtuseta ridu käesoleva veeru jaoks.</td>
</tr>
<tr>
<td>(<span class="code">Finantside ja toimingute päring</span>) (sulgude vaheline finantside ja toimingute päring)</td>
<td>Kirjeldatud päringule vastav</td>
<td>Tippige sulgude vahele päring SQL-lausena, kasutades päringukeelt Finantsid ja toimingud.</td>
  <td><strong><span class="code">((AccountNum NAGU "US *") & & (DirPartyTable.Name NAGU "CONT*"))</span></strong><br><br> 
       filtritingimuse süntaksi näitena väljal juurandmeallikast, samuti väljal teisest andmeallikast (kõigi klientide lehel)</td>
</tr>
<tr>
<td>N</td>
<td>Tänane kuupäev</td>
<td>Tippige <strong>T</strong>.</td>
<td><strong>T</strong> vastab tänasele kuupäevale.</td>
</tr>
<tr>
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong>-meetod sulgudes)</td>
<td>Vastendab <strong>SysQueryRangeUtil</strong>-meetodi parameetritega määratud väärtuse või väärtusevahemiku</td>
<td>Tippige <strong>SysQueryRangeUtil</strong>-meetod, mille parameetrid määravad väärtuse või väärtusevahemiku.</td>
<td>
<ol>
<li>Klõpsake valikuid <strong>Müügireskontro</strong> &gt; <strong>Arved</strong> &gt; <strong>Ava kliendiarved</strong>.</li>
<li>Vajutage klahvikombinatsiooni Ctrl + Shift + F3, et avada leht <strong>Päring</strong>.</li>
<li>Klõpsake vahekaardil <strong>Vahemik</strong> nuppu <strong>Lisa</strong>.</li>
<li>Valige väljal <strong>Tabel</strong> suvand <strong>Avatud kliendikanded</strong>.</li>
<li>Valige väljal <strong>Väli</strong> suvand <strong>Tähtaeg</strong>.</li>
<li>Sisestage väljale <strong>Kriteeriumid</strong> väärtus <strong>(yearRange(-2,0))</strong>.</li>
<li>Klõpsake nupul <strong>OK</strong>. Loendilehte värskendatakse, et kuvada teie sisestatud kriteeriumitele vastavad arved. Selle näite puhul loetletakse kahe eelmise aasta tasumata arved.</li>
</ol>
Lisateavet <strong>SysQueryRangeUtil</strong>-kuupäevameetodite kohta ja mõne näite leiate järgmises jaotises toodud tabelist.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Täpsemad kuupäevapäringud, mis kasutavad SysQueryRangeUtil-meetodeid

<table>
<thead>
<tr>
<th>Meetod</th>
<th>Kirjeldus</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr>
<td>Day (_relativeDays=0)</td>
<td>Leidke seansi kuupäevaga seotud kuupäev. Positiivsed väärtused näitavad tulevikukuupäevi ja negatiivsed väärtused näitavad minevikukuupäev.</td>
<td>
<ul>
<li><strong>Homme</strong> – sisestage <strong>(Day(1))</strong>.</li>
<li><strong>Täna</strong> – sisestage <strong>(Day(0))</strong>.</li>
<li><strong>Eile</strong> – sisestage <strong>(Day(-1))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Leidke seansi kuupäevaga seotud kuupäevavahemik. Positiivsed väärtused näitavad tulevikukuupäevi ja negatiivsed väärtused näitavad minevikukuupäev.</td>
<td>
<ul>
<li><strong>Viimased 30 päeva</strong> – sisestage <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Eelmised 30 päeva ja järgmised 30 päeva</strong> – sisestage <strong>(DayRange(-30,30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Leidke kõik kuupäevad pärast määratud suhtelist kuupäeva.</td>
<td>
<ul>
<li><strong>Rohkem kui 30 päeva alates praegusest</strong> – sisestage <strong>(GreaterThanDate(30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Leidke kõik kuupäeva-/kellaajakirjed pärast praegust aega.</td>
<td>
<ul>
<li><strong>Kõik tuleviku kuupäevad/kellaajad</strong> – sisestage <strong>(GreaterThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Leidke kõik kuupäevad enne määratud suhtelist kuupäeva.</td>
<td>
<ul>
<li><strong>Vähem kui seitse päeva alates praegusest</strong> – sisestage <strong>(LessThanDate(7))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Leidke kõik kuupäeva-/kellaajakirjed enne praegust aega.</td>
<td>
<ul>
<li><strong>Kõik varasemad kuupäevad/kellaajad</strong> – sisestage <strong>(LessThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Leidke kuupäevavahemik praeguse kuuga seotud kuude põhjal.</td>
<td>
<ul>
<li><strong>Eelmised kaks kuud</strong> – sisestage <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Järgmised kolm kuud</strong> – sisestage <strong>(MonthRange(0,3))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Leidke kuupäevavahemik praeguse aastaga seotud aastate põhjal.</td>
<td>
<ul>
<li><strong>Järgmine aasta</strong> – sisestage <strong>(YearRange(0, 1))</strong>.</li>
<li><strong>Eelmine aasta</strong> – sisestage <strong>(YearRange(-1,0))</strong>.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]