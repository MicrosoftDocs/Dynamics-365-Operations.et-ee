---
title: Tagastatud kaupade likvideerimise viisi määratlemine
description: Määratlege tagastatud kaupade likvideerimise viis.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb991b5e9abbe517dcbd73de4f34744955383e82
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206653"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Tagastatud kaupade likvideerimise viisi määratlemine 

[!include [banner](../includes/banner.md)]


Kui töötlete tagastuskorraldust, peate määrama põhjusekoodi selgitamaks, miks toode tagastatakse. Peate määrama ka likvideerimiskoodi ja likvideerimistegevuse, et määratleda, mida teha tagastatud tootega.

Likvideerimiskoodi saab rakendada, kui loote tagastustellimuse, registreerite kauba saabumise või kauba saabumise saatelehe uuenduse ja lõpetate vahelao orderi.

Saate määratleda kõiki likvideerimiskoode, mida äriprotsessi toetamiseks tarvis. Järgnev tabel annab tavaliselt kasutatavate koodide komplekti, et määrata tagastatud kauba likvideerimine.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Likvideerimise tüüp</p></th>
<th><p>Tavaline kood</p></th>
<th><p>Kirjeldus</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Likvideerimine</p></td>
<td><p>SC</p></td>
<td><p>Mahakandmine/Hävitamine</p></td>
</tr>
<tr class="even">
<td><p>Likvideerimine</p></td>
<td><p>DC</p></td>
<td><p>Annetamine heategevuseks</p></td>
</tr>
<tr class="odd">
<td><p>Likvideerimine</p></td>
<td><p>TD</p></td>
<td><p>Kolmanda osapoole likvideerimine</p></td>
</tr>
<tr class="even">
<td><p>Likvideerimine</p></td>
<td><p>SL</p></td>
<td><p>Jääkväärtus</p></td>
</tr>
<tr class="odd">
<td><p>Likvideerimine</p></td>
<td><p>TS</p></td>
<td><p>Kolmanda osapoole müük (teisejärgulised turud)</p></td>
</tr>
<tr class="even">
<td><p>Paranda/Muuda</p></td>
<td><p>RW</p></td>
<td><p>Taastöötlus</p></td>
</tr>
<tr class="odd">
<td><p>Paranda/Muuda</p></td>
<td><p>RF</p></td>
<td><p>Taastootmine/Remontimine</p></td>
</tr>
<tr class="even">
<td><p>Paranda/Muuda</p></td>
<td><p>MD</p></td>
<td><p>Muuda</p></td>
</tr>
<tr class="odd">
<td><p>Paranda/Muuda</p></td>
<td><p>RP</p></td>
<td><p>Remont</p></td>
</tr>
<tr class="even">
<td><p>Paranda/Muuda</p></td>
<td><p>RV</p></td>
<td><p>Tagasta tarnijale</p></td>
</tr>
<tr class="odd">
<td><p>Muu</p></td>
<td><p>AI</p></td>
<td><p>Kasuta nii, nagu on</p></td>
</tr>
<tr class="even">
<td><p>Muu</p></td>
<td><p>RS</p></td>
<td><p>Uuestimüük</p></td>
</tr>
<tr class="odd">
<td><p>Muu</p></td>
<td><p>EX</p></td>
<td><p>Rahavahetus</p></td>
</tr>
<tr class="even">
<td><p>Muu</p></td>
<td><p>MS</p></td>
<td><p>Muud</p></td>
</tr>
</tbody>
</table>


Iga määratletava likvideerimistähise jaoks peate valima likvideerimistegevuse. Likvideerimistegevus määrab likvideerimiskoodide füüsilised ja majanduslikud mõjud. Näiteks määrab likvideerimisetegevus tagastatud füüsilise käitlemise, tagastatud kauba rahalise mõju ja kas kliendile tuleb saata asenduskaup. Saate määrata piiramatu arvu likvideerimiskoode vastavalt oma ettevõtte vajadustele, kuid on olemas ainult kuus eelmääratletud likvideerimistegevust, mida saab valida. Järgnev tabel annab likvideerimistegevused ja nende definitsioonid.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Likvideerimistegevus</p></th>
<th><p>Kirjeldus</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Krediit</strong></p></td>
<td><p>Tagastage kaup varudesse ja tagastage kliendile makse.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ainult kreedit</strong></p></td>
<td><p>Kliendile tagastatakse makse ilma kauba tagastamist nõudmata või eeldamata.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Praak</strong></p></td>
<td><p>Lugege kaup praagiks ja tagastage kliendile makse.</p></td>
</tr>
<tr class="even">
<td><p><strong>Asenda ja kanna kreeditisse</strong></p></td>
<td><p>Tagastage kaup varudesse, looge asenduskorraldus ja tagastage kliendile makse.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Asenda ja kanna praaki</strong></p></td>
<td><p>Lugege kaup praagiks, looge asendamiskorraldus ja tagastage kliendile makse.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tagasta kliendile</strong></p></td>
<td><p>Lükake kauba tagastamine tagasi ja tagastage see kliendile.</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Likvideerimiskoodi valimine vahelao orderile

1.  Klõpsake valikuid **Varude haldamine** \> **Perioodiline** \> **Kvaliteedijuhtimine** \> **Vahelao orderid**.

2.  Olemasoleva vahelao orderi jaoks valige tegevus väljalt **Likvideerimiskood** vahekaardil **Ülevaade**.



## <a name="see-also"></a>Vt ka

[Vahelao order (vorm)](https://technet.microsoft.com/library/aa554073(v=ax.60))

[Likvideerimiskoodid (vorm)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  


