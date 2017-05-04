---
title: "Varuobjekti väärtused"
description: "Selles artiklis antakse teavet lao objekti väärtuste arvutamise kohta."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Varuobjekti väärtused

Selles artiklis antakse teavet lao objekti väärtuste arvutamise kohta. 

Uus funktsioon nimega **füüsiline kogus **võimaldab näha konkreetse varuobjekti väärtusi. Kuluobjekt tähistab üksuse taset, kus laoarvestus toimub. Lisateavet kuluobjektide kohta leiate jaotisest [Kuluobjektid](cost-object.md). Konkreetse varuobjekti väärtuste vaatamiseks klõpsake lehel **Kuluobjekt** valikut **Füüsiline kogus**. Varuobjekti väärtus arvutatakse nii: varuobjekti väärtus = kuluobjekti keskmine ühiku maksumus × varuobjekti kogus. Järgmine näide illustreerib, kuidas varuobjekti ja kuluobjekti väärtused arvutatakse. Kaubale A registreeritakse kaks toote sissetuleku sündmust:

-   Toote sissetulek 1: kogus = 100 tk, summa = 1000.00 $, koht = 1, ladu = 11, partii nr = B1
-   Toote sissetulek 2: kogus = 50 tk, summa = 800.00 $, koht = 1, ladu = 11, partii nr = B2

Järgmises tabelis on kuluobjekti arvutuse tulemus. Tulemust saab vaadata lehel **Kuluobjekt**.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekti tüüp</th>
<th>Kaubakood</th>
<th>Laoala</th>
<th>Kogus</th>
<th>Laoühik</th>
<th>Väärtus</th>
<th>Keskmine ühikukulu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kuluobjekt</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>Kogus</td>
<td><p>$1800.00</p></td>
<td><p>$12.00</p></td>
</tr>
</tbody>
</table>

Järgmises tabelis on varuobjekti arvutuse tulemus. Tulemust saab vaadata, klõpsates nuppu **Füüsiline kogus** lehel **Kuluobjekt**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekti tüüp</th>
<th>Kaubakood</th>
<th>Laoala</th>
<th>Ladu</th>
<th>Partii nr</th>
<th>Kogus</th>
<th>Laoühik</th>
<th>Väärtus</th>
<th>Keskmine ühikukulu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Varuobjekt</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Kogus</td>
<td><p>$1200.00</p></td>
<td><p>$12.00</p></td>
</tr>
<tr class="even">
<td>Varuobjekt</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Kogus</td>
<td><p>$600.00</p></td>
<td><p>$12.00</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Vt ka
--------

[Kuluobjektid](cost-object.md)

[Kulukirjed](cost-entries.md)

[Mida on Microsoft Dynamics AX-is uut ja mis on muutunud?](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


