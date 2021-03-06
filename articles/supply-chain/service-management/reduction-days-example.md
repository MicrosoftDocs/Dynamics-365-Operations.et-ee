---
title: Vähendamispäevade näide
description: Vähendamispäevade näide,
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836058"
---
# <a name="reduction-days-example"></a>Vähendamispäevade näide 

[!include [banner](../includes/banner.md)]


Olete loonud kordustellimuse kande kliendi kordustellimuse haldamiseks, nagu kirjeldatud järgmises tabelis.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Kuupäevast</p></th>
<th><p>Kuupäevani</p></th>
<th><p>Korduv tellimus</p></th>
<th><p>Kordustellimuse tüüp</p></th>
<th><p>Project</p></th>
<th><p>Kategooria</p></th>
<th><p>Müügivaluuta</p></th>
<th><p>Müügihind</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01. märts 2011</p></td>
<td><p>31. märts 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Tavaline</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p> eurot</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Klient teatab, et ei vaja teenust kahel päeval (10. ja 11. märtsil). Nõustute vähendama kordustellimust nende kahe päeva võrra.

Loote uue, tüübi **Vähendamispäevad** kande, nagu kirjeldatud järgmises tabelis.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Kuupäevast</p></th>
<th><p>Kuupäevani</p></th>
<th><p>Korduv tellimus</p></th>
<th><p>Kordustellimuse tüüp</p></th>
<th><p>Project</p></th>
<th><p>Kategooria</p></th>
<th><p>Müügivaluuta</p></th>
<th><p>Müügihind</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10. märts 2011</p></td>
<td><p>11. märts 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Vähendamispäevad</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p> eurot</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


Kui 2011. aasta märtsi kanded arveldatakse, vähendatakse müügihinda 200 eurot 12.90 euro võrra. Kordustellimuse kande arveldatav summa on seega 187.10 eurot ja kahe kande eest esitatakse kokku arve summas 187.10 eurot.

## <a name="see-also"></a>Vt ka

[Kordustellimuste tasude päevade vähendamine](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]