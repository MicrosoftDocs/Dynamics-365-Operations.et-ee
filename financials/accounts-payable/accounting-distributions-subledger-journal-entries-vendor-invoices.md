---
title: "Arvestuse jaotused ja alammooduli töölehe kirjed hankijaarvete puhul"
description: "Arvestuse jaotuste abil saate määratleda, kuidas summat arvestatakse, näiteks kulude, maksude või tasude arvestamisel hankija arvel. Igal summal, mida tuleb hankija arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 35133c305457b53abdf761f7fd557bf81bc28cde
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a>Arvestuse jaotused ja alammooduli töölehe kirjed hankijaarvete puhul

[!include[banner](../includes/banner.md)]


Arvestuse jaotuste abil saate määratleda, kuidas summat arvestatakse, näiteks kulude, maksude või tasude arvestamisel hankija arvel. Igal summal, mida tuleb hankija arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust. 

<a name="accounting-distributions"></a>Arvestuse jaotused 
-------------------------

Saate kasutada lehel Hankija arve iga hankija arve summa arvestuse jaotuse vaatamiseks ja võimaluse korral muutmiseks järgmisi nuppe.
-   **Summade jaotamine** – saate kuvada ja muuta arvestuse jaotusi üksiku rea ja alamüksuste ridade kohta (nt maksud või tasud). Saate kuvada ja muuta ka alamrea arvestuse jaotusi otse lehelt Käibemaksukanded või Tasude kanded.
    -   Hankija arve päise summad, nt tasud või valuuta ümardamissummad.
    -   Hankija arve rea summade muutmine.
-   **Jaotuste kuvamine**– saate kuvada arvestuste jaotused kõigi dokumendi ridade kohta. Selles vaates arvestuse jaotusi muuta ei saa.
    -   Päise ja rea summade vaatamine.

Kui hankija arve viitab ostutellimusele, saate tükeldada ja muuta arvestuse jaotusi ridade puhul, mis sisaldavad ladustamata kaupa. Kui hankija arve rida ei viita ostutellimuse reale, saate ka arvestuse jaotuse kustutada. Tasude, maksude ja rea allahindluste ridu ei saa tükeldada ega kustutada. Saate pearaamatukontot muuta, kuid te ei saa muuta summasid ega protsente.
> [!NOTE]                                                                                                                                 
> Kui peamine rida sisaldab üksust, mida pole ladustatud, ja arvestuse jaotused on tükeldatud, tükeldatakse alamüksuse read automaatselt nii, et need vastaksid peamise rea finantsdimensioonidele. Alamüksuse rea arvestuse jaotusi ei saa täiendavalt tükeldada ega kustutada, kuid sõltuvalt alamüksuse seadistusest võib teil olla võimalik muuta alamüksuse rea arvestuse jaotuse pearaamatukontot.

## <a name="distributing-amounts"></a>Summade jaotamine
Hankija arve sisestamisel jaotatakse iga summa järgmiselt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Hankija arve rea tüüp</th>
<th>Prioriteetsusjärjestus, mis määrab, kust põhikonto kuvatakse</th>
<th>Prioriteetsusjärjestus, mis määrab, milline finantsdimensiooni vaikeväärtus kuvatakse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ladustatav toode</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus.</li>
<li>Põhikonto väli, kui lehel Sisestamine on valitud suvand Toote ostukulu.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Saate kasutada hankija arve finantsdimensiooni väärtusi.</li>
</ol></td>
</tr>
<tr class="even">
<td>Hankekategooria või toode, mis pole ladustatud</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui hankija arve rida viitab ostutellimuse reale.</li>
<li>Põhikonto väli, kui lehel Sisestamine on valitud suvand Kulu ostukulu.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</li>
<li>Saate kasutada hankija arve finantsdimensiooni väärtusi.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Põhivarad</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui hankija arve rida viitab ostutellimuse reale.</li>
<li>Põhikonto väli, kui vormi Hankija arve väljal Kande tüüp on valitud suvand Soetus ja lehel Põhivara sisestusreeglid valitakse suvand Soetus.</li>
<li>Põhikonto väli, kui vormi Hankija arve väljal Kande tüüp on valitud suvand Soetuse korrigeerimine ja lehel Põhivara sisestusreeglid valitakse suvand Soetuse korrigeerimine.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="even">
<td>Hankija arve real määratletud projekt</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</li>
<li>Põhikonto väli, kui lehe Projektigrupid väljal Sisesta kulud – kaup on valitud suvand Saldo ja lehel Pearaamatu sisestamise seadistus valitakse suvand Kulu.</li>
<li>Põhikonto väli, kui lehe Projektigrupid väljal Sisesta kulud – kaup on valitud suvand Kasub ja kahjum ning lehel Pearaamatu sisestamise seadistus valitakse suvand Kulu – kaup.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rea allahindlus</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</li>
<li>Põhikonto väli, kui lehel Sisestamine valitakse suvand Allahindlus.</li>
<li>Kui allahindluse põhikonto pole sisestusreeglites määratletud, siis laiendatud hinna arvestuse jaotus ostutellimuse real.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul arvestuse jaotust.</li>
<li>Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve real finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="even">
<td>Ostukulu, mis sisestatakse ostutellimuse rea vahekaardile Hind ja allahindlus</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</li>
<li>Laiendatud hinna arvestuse jaotus ostutellimuse real.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Reatasu</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</li>
<li>Deebetkonto väli lehel Tasukood, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Pearaamatukonto.</li>
<li>Laiendatud hinna arvestuse jaotus ostutellimuse real, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Kaup.</li>
<li>Kreeditkonto väli lehel Tasukood, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Klient/hankija.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="even">
<td>Maks, järgmise tingimusega.
<ul>
<li>Lehel Pearaamatu parameetrid on märgitud ruut Rakenda USA maksureeglid.</li>
</ul></td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</li>
<li>Laiendatud hinna või tasu arvestuse jaotus.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Maks, järgmiste tingimustega.
<ul>
<li>Lehel Pearaamatu parameetrid on tühjendatud ruut Rakenda USA maksureeglid.</li>
<li>Lehel Käibemaksugrupid on käibemaksugrupi puhul ruut Kasuta maksu tühjendatud.</li>
</ul></td>
<td><ol>
<li>Väli Saadaolev käibemaks lehel Pearaamatu sisestusgrupid, kui maksusumma on tagastatav.</li>
<li>Kui maksusumma pole tagastatav, siis laiendatud hind või tasu arvestuse jaotus.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea tasu puhul laiendatud hinna või arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="even">
<td>Maks, järgmiste tingimustega.
<ul>
<li>Lehel Pearaamatu parameetrid on tühjendatud ruut Rakenda USA maksureeglid.</li>
<li>Lehel Käibemaksugrupid on käibemaksugrupi puhul ruut Kasuta maksu märgitud.</li>
</ul></td>
<td><ol>
<li>Väli Saadaolev käibemaks lehel Pearaamatu sisestusgrupid, kui maksusumma on tagastatav.</li>
<li>Väli Kasutusmaksu kulu lehel Pearaamatu sisestusgrupid, kui maksusumma ei ole tagastatav.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea tasu puhul laiendatud hinna või arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Päise tasu</td>
<td><ol>
<li>Deebetkonto väli lehel Tasukood, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Pearaamatukonto.</li>
<li>Kreeditkonto väli lehel Tasukood, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Klient/hankija.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</li>
<li>Saate kasutada hankija arve päise finantsdimensiooni vaikemalli väärtusi.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="even">
<td>Päise allahindlus</td>
<td><ol>
<li>Põhikonto väli lehe Automaatsete kannete kontod sisestustüübi Hankija arve allahindlus puhul.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
</tbody>
</table>

 
<a name="distributing-taxes"></a>Maksude jaotamine
------------------

Maksude arvestuse jaotusi ei saa luua, kuni makse arvutatakse. Käibemaksu arvutamiseks peate täitma lehel Hankija arve ühe järgmise ülesande.
-   Arve kogusumma kuvamine.
-   Käibemaksu kuvamine.
-   Alammooduli töölehe kuvamine.
-   Hankija koguarve arvestuse jaotuste kuvamine.
-   Hankija arve ootele panemine.
-   Hankija arve sisestamine.

## <a name="subledger-journals-for-vendor-invoices"></a>Hankija arvete alammooduli töölehed
Enne hankija arve sisestamist saate vaadata arve täielikku raamatupidamiskirjet, mis sisaldab deebet- ja kreeditsummasid, kontrollimaks, et arve sisestatakse õigetele kontodele. Selles vaates nimetatakse täielikku raamatupidamiskirjet alammooduli tööleheks. 

Kui alammooduli töölehe kirje on enne hankija arve töölehele paigutamist vale, ei saa te alammooduli töölehe kirjet muuta. Selle asemel peate muutma arvestuse jaotusi või sisestusreegleid. Arvestuse jaotuste abil määratletakse raamatupidamiskirje üks pool, deebet- või kreeditsumma. Alammooduli töölehe konto kirje vastaskonto luuakse sisestusreegleid kasutades, nt hankija konto või maksu põhjal.






