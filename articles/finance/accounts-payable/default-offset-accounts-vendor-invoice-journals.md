---
title: Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod
description: See teema aitab teil otsustada, kuhu peaksite arve töölehtede vaikekontod määrama.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6ff4e209f1d1c41d7c05cad735aacc320bdeb83
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189679"
---
# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod

[!include [banner](../includes/banner.md)]

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
<td><strong>Töölehe nimed</strong> – seadistage töölehtede vaikevastaskontod leheküljel <strong>Töölehe nimed</strong>. Valige suvand <strong>Fikseeritud vastaskonto</strong>. Pange tähele, et te ei saa määrata vaikevastaskontosid töölehe nimedele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</td>
<td><ul>
<li>Töölehe päis, mis kasutab töölehe nime</li>
<li>Töölehekanded töölehe nime kasutavatel töölehtedel</li>
</ul></td>
<td>Kui lehel <strong>Töölehe nimed</strong> on valitud suvand <strong>Fikseeritud vastaskonto</strong>, tühistab töölehe nime vastaskonto hankija või hankijategrupi vaikevastaskonto.</td>
<td>Selle valiku abil saate seadistada spetsiifiliste väljaminekute ja kulude töölehed, mis arvestatakse konkreetsetele kontodele, olenemata hankijast või hankijagrupist, millesse hankija kuulub.</td>
</tr>
<tr class="even">
<td><strong>Töölehe nimed</strong> – seadistage töölehtede vaikevastaskontod leheküljel <strong>Töölehe nimed</strong>. Tühjendage suvand <strong>Fikseeritud vastaskonto</strong>. Pange tähele, et te ei saa määrata vaikevastaskontosid töölehe nimedele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</td>
<td><ul>
<li>Töölehe päis</li>
<li>Töölehekanded töölehe nime kasutavatel töölehtedel</li>
</ul></td>
<td>Neid vaikekirjeid kasutatakse töölehe päise lehtedel ja töölehe päise lehel olevat vastaskontot vaikekirjena töölehe kande lehtedel. Vaikekontosid lehel <strong>Töölehe nimed </strong>kasutatakse ainult siis, kui hankijakontole pole vaikekontosid seadistatud.</td>
<td>Selle valiku abil saate seadistada vaikekontod, mida kasutatakse, kui hankija vaikevastaskontot pole määratud.</td>
</tr>
<tr class="odd">
<td><strong>Töölehe päis</strong> – seadistage töölehe vaikevastaskonto töölehe kande lehtedel vaikekirjena. Pange tähele, et te ei saa määrata vaikevastaskontosid töölehe päisele, kui töölehe nimede töölehe tüüp on <strong>Arveregister</strong> või <strong>Kinnitamine</strong>.</td>
<td>Töölehe kanded töölehel</td>
<td>Töölehe vaikevastaskontot kasutatakse töölehe kande lehtedel vaikekirjena.</td>
<td>Selle valiku abil saate kiirendada andmesisestust, kui enamikul töölehe kirjetest on sama vastaskonto.</td>
</tr>
</tbody>
</table>





