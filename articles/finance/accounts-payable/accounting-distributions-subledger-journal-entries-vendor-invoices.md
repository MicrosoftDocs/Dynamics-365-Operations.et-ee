---
title: Arvestuse jaotused ja töölehekirjed hankija arvete puhul
description: Arvestuse jaotuste abil saate määratleda, kuidas summat arvestatakse, näiteks kulude, maksude või tasude arvestamisel hankija arvel. Igal summal, mida tuleb hankija arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358177"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Arvestuse jaotused ja töölehekirjed hankija arvete puhul

[!include [banner](../includes/banner.md)]

Arvestuse jaotuste abil saate määratleda, kuidas summat arvestatakse, näiteks kulude, maksude või tasude arvestamisel hankija arvel. Igal summal, mida tuleb hankija arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust. 

## <a name="accounting-distributions"></a>Arvestuse jaotused 

Saate kasutada lehel Hankija arve iga hankija arve summa arvestuse jaotuse vaatamiseks ja võimaluse korral muutmiseks järgmisi nuppe.
-   **Summade jaotamine** – saate kuvada ja muuta arvestuse jaotusi üksiku rea ja alamüksuste ridade kohta (nt maksud või tasud). Alamrea arvestuse jaotusi saate vaadata ja muuta ka otse käibemaksukannete **leheküljelt** või kulude **kannete leheküljelt**.
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
<li>Põhikonto <strong>väli</strong>, kui lehel Sisestamine on valitud toote ostu <strong></strong> kulu</li>
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
<li>Põhikonto <strong>väli</strong>, kui lehel Sisestamine on valitud kulude ostu <strong></strong> kulu</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</li>
<li>Saate kasutada hankija arve finantsdimensiooni väärtusi.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada kontoplaani leheküljel oleva põhikonto finantsdimensiooni <strong>vaikeväärtusi</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Põhivara</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui hankija arve rida viitab ostutellimuse reale.</li>
<li>Kui <strong>hankija</strong> arve lehe <strong>väljal Kande</strong> tüüp on<strong></strong> valitud soetus, <strong>siis on põhivara sisestusreeglite</strong><strong></strong><strong>lehel valitud põhikonto väli, kui soetus on</strong> valitud.</li>
<li>Kui <strong>väljal Kande</strong> tüüp on valitud <strong>soetamise</strong> korrigeerimine, siis väli Põhikonto, <strong></strong><strong></strong> kui põhivara sisestusreeglite lehel on <strong>valitud soetamise korrigeerimine.</strong></li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada kontoplaani leheküljel oleva põhikonto finantsdimensiooni <strong>vaikeväärtusi</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Hankija arve real määratletud projekt</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</li>
<li>Kui <strong>projektigruppide</strong> lehe väljal <strong>Kulude sisestamine -</strong><strong></strong> kaup on valitud saldo,<strong></strong><strong></strong> siis kui pearaamatu sisestamise häälestuslehel on <strong>valitud väli Kulu põhikonto.</strong></li>
<li>Kui <strong>projektigruppide lehe</strong> väljal <strong>Kulude -</strong><strong></strong> kauba sisestamine on valitud tulu ja kulu, <strong></strong><strong>siis põhikonto väli, kui pearaamatu sisestamisseadistuse lehel on</strong><strong>valitud väärtus Kulu -</strong> kaup.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rea allahindlus</td>
<td><ol>
<li>Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</li>
<li>Väli <strong>Põhikonto</strong>, kui <strong>lehel</strong> Sisestamine on valitud <strong>allahindlus</strong>.</li>
<li>Kui allahindluse põhikonto pole sisestusreeglites määratletud, siis laiendatud hinna arvestuse jaotus ostutellimuse real.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul arvestuse jaotust.</li>
<li>Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve real finantsdimensiooni väärtusi.</li>
<li>Saate kasutada kontoplaani leheküljel oleva põhikonto finantsdimensiooni <strong>vaikeväärtusi</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Ostukulu, mis on sisestatud <strong>ostutellimuse rea vahekaardile</strong> Hind ja allahindlus</td>
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
<li>Kui <strong>pearaamatukonto</strong> on valitud väljal <strong>Deebeti</strong> tüüp lehe Tasud <strong></strong> kood, kuvatakse <strong>kulude</strong> koodi lehe deebetkonto <strong></strong> väli.</li>
<li>Kui <strong>kaup</strong> on valitud <strong>kulude koodi</strong> lehe <strong>deebeti tüübi</strong> väljal, siis laiendatud hinna arvestuse jaotus ostutellimuse real.</li>
<li>Kui <strong>lehe Tasud</strong> kood väljal <strong>Deebeti</strong> tüüp on <strong></strong> valitud klient/hankija, <strong>kuvatakse kulude</strong> koodilehe väli <strong>Kreeditkonto</strong>.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada kontoplaani leheküljel oleva põhikonto finantsdimensiooni <strong>vaikeväärtusi</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Maks, järgmise tingimusega.
<ul>
<li>Suvand <strong>Rakenda USA maksureeglid</strong> valitakse pearaamatu <strong>parameetrite lehel</strong>.</li>
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
<li>Usa <strong>maksureeglite rakendamiseks suvand</strong> tühjendatakse pearaamatu <strong>parameetrite</strong> lehel.</li>
<li>Käibemaksugrupi <strong></strong> kasutusmaksu väli tühjendatakse käibemaksugruppide <strong>lehel</strong>.</li>
</ul></td>
<td><ol>
<li>Kui maksusumma on taastatav, siis väli <strong>Saadaolev käibemaks</strong> pearaamatu sisestusgruppide <strong></strong> lehel.</li>
<li>Kui maksusumma pole tagastatav, siis laiendatud hind või tasu arvestuse jaotus.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea tasu puhul laiendatud hinna või arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada kontoplaani leheküljel oleva põhikonto finantsdimensiooni <strong>vaikeväärtusi</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Maks, järgmiste tingimustega.
<ul>
<li>Usa maksureeglite rakendamiseks suvand tühjendatakse pearaamatu <strong>parameetrite</strong> lehel.</li>
<li>Käibemaksugrupi <strong></strong> kasutusmaksu väli on valitud lehel <strong>Käibemaksugrupid</strong>.</li>
</ul></td>
<td><ol>
<li>Kui maksusumma on taastatav, siis väli <strong>Saadaolev käibemaks</strong> pearaamatu sisestusgruppide <strong></strong> lehel.</li>
<li>Kui maksusumma ei ole tagasisaadav, siis <strong>väli Kasuta</strong> maksukulu pearaamatu sisestamisgruppide <strong></strong> lehel.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea tasu puhul laiendatud hinna või arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada kontoplaani leheküljel oleva põhikonto finantsdimensiooni <strong>vaikeväärtusi</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Päise tasu</td>
<td><ol>
<li>Kui <strong>pearaamatukonto</strong> on valitud väljal <strong>Deebeti</strong> tüüp lehe Tasud <strong></strong> kood, kuvatakse <strong>lehe Tasud</strong><strong>kood väli Deebetkonto</strong>.</li>
<li>Kui <strong>lehe Tasud</strong> kood väljal <strong>Deebeti</strong> tüüp on <strong></strong> valitud klient/hankija, <strong>kuvatakse kulude</strong> koodilehe väli <strong>Kreeditkonto</strong>.</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</li>
<li>Saate kasutada hankija arve päise finantsdimensiooni vaikemalli väärtusi.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada kontoplaani leheküljel oleva põhikonto finantsdimensiooni <strong>vaikeväärtusi</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Päise allahindlus</td>
<td><ol>
<li>Hankija <strong>arve</strong> allahindluse sisestustüübi <strong>põhikonto väli</strong> automaatsete <strong>kannete lehel Kontode</strong> jaoks</li>
</ol></td>
<td><ol>
<li>Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</li>
<li>Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</li>
<li>Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</li>
<li>Saate kasutada kontoplaani leheküljel oleva põhikonto finantsdimensiooni <strong>vaikeväärtusi</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Maksude jaotamine

Maksude arvestuse jaotusi ei saa luua, kuni makse arvutatakse. Käibemaksude arvutamiseks peate hankija arve lehel täitma ühe **järgmistest ülesannetest**:
-   Arve kogusumma kuvamine.
-   Käibemaksu kuvamine.
-   Alammooduli töölehe kuvamine.
-   Hankija koguarve arvestuse jaotuste kuvamine.
-   Hankija arve ootele panemine.
-   Hankija arve sisestamine.

## <a name="subledger-journals-for-vendor-invoices"></a>Hankija arvete alammooduli töölehed
Enne hankija arve sisestamist saate vaadata arve täielikku raamatupidamiskirjet, mis sisaldab deebet- ja kreeditsummasid, kontrollimaks, et arve sisestatakse õigetele kontodele. Selles vaates nimetatakse täielikku raamatupidamiskirjet alammooduli tööleheks. 

Kui alammooduli töölehe kirje on enne hankija arve töölehele paigutamist vale, ei saa te alammooduli töölehe kirjet muuta. Selle asemel peate muutma arvestuse jaotusi või sisestusreegleid. Arvestuse jaotuste abil määratletakse raamatupidamiskirje üks pool, deebet- või kreeditsumma. Alammooduli töölehe konto kirje vastaskonto luuakse sisestusreegleid kasutades, nt hankija konto või maksu põhjal.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
