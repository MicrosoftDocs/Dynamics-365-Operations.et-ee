---
title: Kordustellimuse müügihinnad
description: Kui loote kordustellimuse, tuletatakse müügihind müügihinna seadistusest, mis loodi vormis Müügihind (kordustellimus).
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd63fc290263babafabd6e29441f008d0cf10e13
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569981"
---
# <a name="subscription-sales-prices"></a>Kordustellimuse müügihinnad

[!include [banner](../includes/banner.md)]

Kui loote kordustellimuse, tuletatakse müügihind müügihinna seadistusest, mis loodi vormis **Müügihind (kordustellimus)**.

Vormis **Müügihind (kordustellimus)** saate luua müügihinnad konkreetsele kordustellimusele või luua müügihinnad, mis rakenduvad laiemalt. Selleks et müügihind rakenduks kordustellimusel, peavad kordustellimuse perioodi kood ja valuuta ning müügihinna perioodi kood ja valuuta olema identsed.

Kui perioodi kood ja valuuta on kordustellimusel ja müügihinnal identsed, valitakse kordustellimuse müügihinnad alltoodud tabeli prioriteetide alusel. Tühi lahter tabelis tähistab tühja välja ja X tähistab väärtust, mis on võrdne väärtusega kordustellimuses, millest tehing koostati.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Prioriteet </p></th>
<th><p><strong>Kategooria</strong></p></th>
<th><p><strong>Projekti ID</strong></p></th>
<th><p><strong>Kordustellimus</strong></p></th>
<th><p><strong>Müügivaluuta</strong></p></th>
<th><p><strong>Perioodi kood</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>

Kui luuakse kordustellimuse tasu, valitakse kordustellimuse müügihinnaks kõrgeima detailsustasemega müügihind, nagu ülaltoodud tabelis märgitud.

## <a name="update-and-index-subscription-sales-prices"></a>Kordustellimuste müügihindade uuendamine ja indekseerimine

Saate kordustellimuse müügihinda värskendada värskendades baashinda või indeksit. Saate värskendada protsendi kaupa või uue väärtuseni.

## <a name="subscription-fee-sales-prices"></a>Kordustellimuse tasu müügihinnad

Kui loote kordustellimuse tasu, põhineb müügihind kordustellimuse müügihinna seadistusel. Võite kasutada kas baashinda kordustellimuse hinnaseadistusest või luua indekseeritud müügihinnad.

## <a name="example"></a>Näide

Soovite seadistada uuele projektile 9030 500 euro suurused kordustellimuse müügihinnad. Vormis **Müügihind (kordustellimus)** saate luua kordustellimuse müügihinna rea, nagu näidatud järgmises tabelis.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Kehtiv alates</p></th>
<th><p>Kategooria</p></th>
<th><p>Project</p></th>
<th><p>Korduv tellimus</p></th>
<th><p>Perioodi kood</p></th>
<th><p>Müügivaluuta</p></th>
<th><p>Müügihind</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Kuu</p></td>
<td><p> eurot</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Pange tähele, et väljad **Kategooria** ja **Kordustellimus** on tühjad.

Seejärel loote järgmised kordustellimused.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Teenuse kordustellimus</p></th>
<th><p>Project</p></th>
<th><p>Kordustellimuste grupp</p></th>
<th><p>Kategooria</p></th>
<th><p>Valuuta</p></th>
<th><p>Perioodi kood</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat1</p></td>
<td><p> eurot</p></td>
<td><p>Igakuine</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat2</p></td>
<td><p> eurot</p></td>
<td><p>Igakuine</p></td>
</tr>
</tbody>
</table>


Nüüd loote kordustellimuste tasud mõlemale kordusteelimusele Sub 1 kordustellimuste grupis:

1.  Klõpsake valikuid **Teenuste haldus** \> **Seadistus** \> **Teenuse kordustellimused** \> **Kordustellimuste grupid**.

2.  Klõpsake vormis **Kordustellimuste grupid** valikuid **Funktsioon** \> **Kordustellimuse tasu loomine**.

3.  Sisestage asjakohane teave vormi **Kordustellimuse tasu loomine**. Lisateavet vt teemast [Kordustellimuste tasukannete loomine](create-subscription-fee-transactions.md).

Kordustellimuse tasud, mille müügihind on 500 eurot, luuakse mõlema kordustellimuse jaoks, nagu on näidatud järgmises tabelis.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Projekti kuupäev</p></th>
<th><p>Teenuse kordustellimus</p></th>
<th><p>Project</p></th>
<th><p>Kategooria</p></th>
<th><p>Alguskuupäev</p></th>
<th><p>Lõppkuupäev</p></th>
<th><p>Müügivaluuta</p></th>
<th><p>Müügihind</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01.01.2007</p></td>
<td><p>31.03.2007</p></td>
<td><p> eurot</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28.08.2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01.01.2007</p></td>
<td><p>31.03.2007</p></td>
<td><p> eurot</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Hiljem otsustate, et soovite täpsustada projekti 9030 kategooria SubCat1 müügihindu. Seetõttu loote uue 550 euro suuruse müügihinnaga müügihinna rea projekti 9030 ja tasu kategooria SubCat1 kombinatsiooni jaoks. Nüüd on projekt 9030 jaoks olemas kaks kordustellimuse müügihinna rida, nagu on näidatud järgmises tabelis.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Kehtiv alates</p></th>
<th><p>Kategooria</p></th>
<th><p>Project</p></th>
<th><p>Korduv tellimus</p></th>
<th><p>Perioodi kood</p></th>
<th><p>Valuuta</p></th>
<th><p>Müügihind</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Kuu</p></td>
<td><p> eurot</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28.08.2007</p></td>
<td><p>SubCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>Kuu</p></td>
<td><p> eurot</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>

Kordate ülalkirjeldatud protseduuri, et luua kordustellimuste tasud mõlemale kordustellimusele kordustellimuse grupis Sub1. Järgmises tabelis on näha kanded, mis luuakse kummagi kordustellimuse grupiga seotud kordustellimuse jaoks.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Projekti kuupäev</p></th>
<th><p>Korduv tellimus</p></th>
<th><p>Project</p></th>
<th><p>Kategooria</p></th>
<th><p>Alguskuupäev</p></th>
<th><p>Lõppkuupäev</p></th>
<th><p>Müügivaluuta</p></th>
<th><p>Müügihind</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.07.2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01.01.2008</p></td>
<td><p>31.03.2008</p></td>
<td><p> eurot</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28.07.2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01.01.2008</p></td>
<td><p>31.03.2008</p></td>
<td><p> eurot</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>

Esimeses tehingus kordustellimusele 00020\_135 tuletatakse 550 euro suurune müügihind kordustellimuse müügihinnast, mis on seatud konkreetse projekti ja kategooria kombinatsiooni jaoks. Teises tehingus kordustellimusele 00021\_135 kasutatakse 500 euro suurust müügihinda projekti kordustellimuse müügihinnana, sest projekti 9030 ja kategooria SubCat2 kombinatsioonile pole hinda seatud.

## <a name="see-also"></a>Vt ka

[Kordustellimuste müügihindade uuendamine ja indekseerimine](update-and-index-subscription-sales-prices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
