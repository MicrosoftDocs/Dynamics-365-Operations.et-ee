---
title: "Arvestuse jaotused ja alammooduli töölehe kirjed vabas vormis arvete puhul"
description: "Arvestuse jaotused määratlevad, kuidas summat arvestatakse, näiteks tulu, maksude või tasude arvestamisel vabas vormis arvel. Igal summal, mida tuleb vabas vormis arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b530b5c8b5e252efb253dcf5b4ad080e2f646e5f
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a>Arvestuse jaotused ja alammooduli töölehe kirjed vabas vormis arvete puhul

[!include[banner](../includes/banner.md)]


Arvestuse jaotused määratlevad, kuidas summat arvestatakse, näiteks tulu, maksude või tasude arvestamisel vabas vormis arvel. Igal summal, mida tuleb vabas vormis arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust.

<a name="accounting-distributions"></a>Arvestuse jaotused
------------------------

Saate kasutada järgmisi nuppe lehel Vabas vormis arve iga vabas vormis arve summa arvestuse jaotuse vaatamiseks ja võimaluse korral muutmiseks.

-   **Summade jaotamine** –saate kuvada ja muuta arvestuse jaotusi üksiku rea ning alamridade kohta (nt maksud või tasud). Saate kuvada ja muuta ka alamrea arvestuse jaotusi otse lehelt Käibemaksukanded või Tasude kanded.
    -   Saate vabas vormis arve päise summasid (nt tasusid või valuuta ümardamissummasid) muuta.
    -   Saate vabas vormis arve reasummasid muuta.
-   **Jaotuste kuvamine**–arvestuste jaotuste kuvamine kõigi dokumendi ridade kohta. Selles vaates arvestuse jaotusi muuta ei saa.
    -   Päise ja rea summade vaatamine.

## <a name="distributing-amounts"></a>Summade jaotamine
Vabas vormis arve sisestamisel jaotatakse iga summa järgmiselt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Rahasumma tüüp</th>
<th>Põhikonto kuvamise koht</th>
<th>Prioriteetsusjärjestus, mis määrab, milline finantsdimensiooni vaikeväärtus kuvatakse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vabas vormis arve rida</td>
<td>Vabas vormis arve rea pearaamatukonto.</td>
<td><ol>
<li>Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</li>
<li>Kui põhikonto ei ole eraldamise konto, kasutage vabas vormis arve real finantsdimensiooni vaikemalli.</li>
<li>Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vabas vormis arve rida põhivara numbri ja väärtusmudeli kombinatsiooni jaoks
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Märkus. </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vabas vormis arve real olev põhikonto on põhivara likvideerimiskonto.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Vabas vormis arve rea pearaamatukonto.</td>
<td><ol>
<li>Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Vabas vormis arve allahindluse summa</td>
<td>Kliendi allahindluste välja põhikonto lehel Skontod.</td>
<td><ol>
<li>Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</li>
<li>Kui põhikonto ei ole eraldamise konto, kasutage vabas vormis arve real finantsdimensiooni vaikemalli.</li>
<li>Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vabas vormis arve käibemaksusumma</td>
<td>Tasumisele kuuluva käibemaksu väli lehel Pearaamatu sisestamisgrupid.</td>
<td><ol>
<li>Kasutage vabas vormis arve rea summas või tasurea summa jaotustes määratud finantsdimensioone.</li>
<li>Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Vabas vormis arve tasurea summa</td>
<td>Väli Kreeditkonto lehel Tasukood.</td>
<td><ol>
<li>Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</li>
<li>Kui põhikonto ei ole eraldamise konto, kasutage vabas vormis arve real finantsdimensiooni vaikemalli.</li>
<li>Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</li>
<li>Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Maksude jaotamine
Maksude arvestuse jaotusi ei saa luua, kuni makse arvutatakse. Käibemaksu arvutamiseks peate täitma ühe järgmise ülesande vabas vormis arve vormil.
-   Käibemaksu kuvamine.
-   Arve kogusumma kuvamine.
-   Saate kuvada rahavoo.
-   Saate kuvada kogu vabas vormis arve arvestuse jaotused.
-   Alammooduli töölehe kuvamine.

## <a name="subledger-journals-for-free-text-invoices"></a> Vabas vormis arvete alammooduli töölehed
Enne vabas vormis arve sisestamist saate vaadata arve täielikku raamatupidamiskirjet, mis sisaldab deebet- ja kreeditsummasid, kontrollimaks, et arve sisestatakse õigetele kontodele. Selles vaates nimetatakse täielikku raamatupidamiskirjet alammooduli tööleheks. Kui alammooduli töölehe kirje on enne vabas vormis arve töölehele paigutamist vale, ei saa alammooduli töölehe kirjet muuta. Selle asemel peate muutma arvestuse jaotusi või sisestusreegleid. Arvestuse jaotuste abil määratletakse raamatupidamiskirje üks pool, deebet- või kreeditsumma. Alammooduli töölehe konto kirje vastaskonto luuakse sisestusreeglite abil, nt kliendi konto või maksu põhjal.




