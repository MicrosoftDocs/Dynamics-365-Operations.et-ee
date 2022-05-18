---
title: Varuobjekti väärtused
description: Selles artiklis antakse teavet lao objekti väärtuste arvutamise kohta.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a5dd487b9213f8f1289412a6a7b8112e6b57df6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670380"
---
# <a name="inventory-object-values"></a>Varuobjekti väärtused

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet lao objekti väärtuste arvutamise kohta. 

Uus funktsioon nimega **füüsiline kogus** võimaldab näha konkreetse varuobjekti väärtusi. 

Kuluobjekt tähistab üksuse taset, kus laoarvestus toimub. Lisateavet kuluobjektide kohta leiate jaotisest [Kuluobjektid](cost-object.md). 

Konkreetse varuobjekti väärtuste vaatamiseks klõpsake lehel **Kuluobjekt** valikut **Füüsiline kogus**. Varude objekti väärtus arvutatakse järgmiselt. 

Varude objekt.Väärtus = Kuluobjekt.Keskmine ühikukulu × Varude objekt.Kogus 

Järgmises näites kirjeldatakse varude objekti ja kuluobjekti väärtuste arvutamist. Kaubale A registreeritakse kaks toote sissetuleku sündmust:

-   Toote sissetulek 1: kogus = 100 tk, summa = 1000.00 $, koht = 1, ladu = 11, partii nr = B1
-   Toote sissetulek 2: kogus = 50 tk, summa = 800.00 $, koht = 1, ladu = 11, partii nr = B2

Järgmises tabelis on kuluobjekti arvutuse tulemus. Tulemust saab vaadata lehel **Kuluobjekt**.

<table>
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

<table>
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



## <a name="additional-resources"></a>Lisaressursid

[Kuluobjektid](cost-object.md)

[Kulukirjed](cost-entries.md)

[Mis on uus ja muudetud](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]