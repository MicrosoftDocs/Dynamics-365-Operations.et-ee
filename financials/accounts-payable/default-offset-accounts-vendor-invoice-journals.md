---
title: "Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod"
description: 
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4691ac4456b08084bcd93f7a8447719a15299c93
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod

[!include[banner](../includes/banner.md)]




Vaikevastaskontosid kasutatakse järgmistel hankija arve töölehe lehekülgedel:

-   Arve tööleht
-   Arve kinnitamise tööleht

Kasutage järgmist tabelit, mis aitab teil otsustada, kuhu peaksite arve töölehtede vaikekontod määrama.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Seadistage vaikekontod siin</th>
<th>Kus vaikekontod saadaval on?</th>
<th>Kuidas see valik mõjutab töötlemist?</th>
<th>Millal peaksite seda valikut kasutama?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Hankijagrupp</strong> – seadistage hankijagruppide vaikevastaskontod leheküljel <strong>Kontode vaikeseadistus</strong>, mille saate avada lehelt <strong>Hankijagrupid</strong>.</td>
<td><ul>
<li>Hankija konto</li>
<li>Hankijagrupi hankija kontode töölehe kanded, kui hankijakontodele pole vaikekontosid määratud</li>
</ul></td>
<td>Hankijagruppide vaikevastaskontod on näidatud hankijate vaikevastaskontodena lehel <strong>Kontode vaikeseadistus</strong>. Selle lehe saate avada loendilehelt <strong>Kõik hankijad</strong>.</td>
<td>Valige see suvand, kui te tavaliselt aja jooksul maksate sama tüüpi asjad eest samadele hankijagruppidele.</td>
</tr>
<tr class="even">
<td><strong>Hankija konto</strong> – seadistage hankija kontode vaikekontod leheküljel <strong>Kontode vaikeseadistus</strong>, mille saate avada lehelt <strong>Hankijad</strong>.</td>
<td>Hankijakonto töölehekanded</td>
<td>Hankijakontode vaikevastaskontod on näidatud hankijakonto töölehekannete vaikevastaskontodena.</td>
<td>Valige see suvand, kui te tavaliselt aja jooksul maksate sama tüüpi asjad eest samadele hankijatele.</td>
</tr>
<tr class="odd">
<td><strong>Töölehe nimed</strong> – seadistage töölehtede vaikevastaskontod leheküljel <strong>Töölehe nimed</strong>. Valige suvand <strong>Fikseeritud vastaskonto</strong>. Pange tähele, et ei saa määrata vaikevastaskontosid töölehe nimedele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</td>
<td><ul>
<li>Töölehe päis, mis kasutab töölehe nime</li>
<li>Töölehekanded töölehe nime kasutavatel töölehtedel</li>
</ul></td>
<td>Kui lehel <strong>Töölehe nimed</strong> on valitud suvand <strong>Fikseeritud vastaskonto</strong>, tühistab töölehe nime vastaskonto hankija või hankijategrupi vaikevastaskonto.</td>
<td>Selle valiku abil saate seadistada spetsiifiliste väljaminekute ja kulude töölehed, mis arvestatakse konkreetsetele kontodele, olenemata hankijast või hankijagrupist, millesse hankija kuulub.</td>
</tr>
<tr class="even">
<td><strong>Töölehe nimed</strong> – seadistage töölehtede vaikevastaskontod leheküljel <strong>Töölehe nimed</strong>. Tühjendage suvand <strong>Fikseeritud vastaskonto</strong>. Pange tähele, et ei saa määrata vaikevastaskontosid töölehe nimedele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</td>
<td><ul>
<li>Töölehe päis</li>
<li>Töölehekanded töölehe nime kasutavatel töölehtedel</li>
</ul></td>
<td>Neid vaikekirjeid kasutatakse töölehe päise lehtedel ja töölehe päise lehel olevat vastaskontot vaikekirjena töölehe kande lehtedel. Vaikekontosid lehel <strong>Töölehe nimed </strong>kasutatakse ainult siis, kui hankijakontole pole vaikekontosid seadistatud.</td>
<td>Selle valiku abil saate seadistada vaikekontod, mida kasutatakse, kui hankija vaikevastaskontot pole määratud.</td>
</tr>
<tr class="odd">
<td><strong>Töölehe päis</strong> – seadistage töölehe vaikevastaskonto töölehe kande lehtedel vaikekirjena. Pange tähele, et ei saa määrata vaikevastaskontosid töölehe päisele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</td>
<td>Töölehe kanded töölehel</td>
<td>Töölehe vaikevastaskontot kasutatakse töölehe kande lehtedel vaikekirjena.</td>
<td>Selle valiku abil saate kiirendada andmesisestust, kui enamikul töölehe kirjetest on sama vastaskonto.</td>
</tr>
</tbody>
</table>






