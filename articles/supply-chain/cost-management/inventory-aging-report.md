---
title: Varude ajalise jaotuse aruande näited ja loogika
description: Selles teemas on toodud näited selle kohta, kuidas tõlgendada varude ajalise jaotuse aruande tulemusi.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983921"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Varude ajalise jaotuse aruande näited ja loogika

[!include [banner](../includes/banner.md)]

Selles teemas on toodud näited selle kohta, kuidas tõlgendada **varude ajalise jaotuse** aruande tulemusi. See aruanne jagab valitud kauba või kaubagrupi laos oleva koguse ja laoväärtused mitmeks perioodiks. Teema hõlmab ka aruande sisemist loogikat.

Selles teemas on toodud näited, mis sisalduvad standardses **varude ajalise jaotuse** aruandes. Siiski soovitame üldiselt kasutada selle aruande versiooni [Varude ajalise jaotuse aruande talletamine](inventory-aging-report-storage.md), eriti kui te peate töötlema palju kaupu ja ladusid. Varude ajalise jaotuse aruande talletamine salvestab kõik teie loodud aruanded, kuvab tulemused interaktiivse lehena ja diagrammina ning võimaldab teil eksportida kõiki salvestatud aruandeid.

## <a name="sample-data-that-is-used-in-these-examples"></a>Näidetes kasutatavad näidisandmed

Teema näited põhinevad selles jaotises kirjeldatud laokannete näidisandmetel.

### <a name="storage-dimension-setup"></a>Laoala dimensiooni seadistamine

Näidissüsteemis on laoala dimensioonid sätestatud järgmiselt.

| Nimi      | Aktiivne | Füüsiline ladu | Finantsiline laovaru |
|-----------|--------|--------------------|---------------------|
| Koht      | Jah    | Jah                | Jah                 |
| Ladu | Jah    | Jah                | Ei                  |

### <a name="inventory-model"></a>Laomudel

Näidissüsteemi puhul on väljastatud toodete laomudel *FIFO* ning laomudeli sätte **Omahind** väärtus on *Kaasa füüsiline väärtus*.

### <a name="inventory-transactions"></a>Laokanded

Väljastatud toote, mille kaubakood on *1000*, puhul on näidissüsteemis järgmised laokanded.

| Viide      | Koht | Ladu | Sissetulek   | Väljastus | Füüsiline kuupäev | Finantskuupäev | Kogus | Sisseostuhind | Füüsiline omahind |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Ostutellimus | 1    | 11        | Ostetud |       | 15. märts      | 15. märts       | 10       | 1000       | 1000                |
| Ostutellimus | 2    | 21        | Ostetud |       | 15. märts      | 15. märts       | 10       | 2,000       | 2,000                |
| Ostutellimus | 1    | 11        | Vastuvõetud  |       | 15. aprill      |                | 5        |             | 375                  |
| Üleviimistellimus | 1    | 11        |           | Müüdud  | 2. mai         | 2. mai          | -5       | -458,33     | -458,33              |
| Üleviimistellimus | 1    | 12        | Ostetud |       | 2. mai         | 2. mai          | 5        | 458.33      | 458.33               |
| Müügitellimus    | 1    | 12        |           | Müüdud  | 3. mai         | 3. mai          | –1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Kuidas arvutatakse igas perioodis koguseid ja summasid?

Eelmistes jaotistes kirjeldatud näidisandmete abil saate käivitada **varude ajalise jaotuse** aruande, millel on järgmised sätted.

- **Kuupäevaga:** *9. mai 2020*
- **Koht:** *Kuva*
- **Ladu:** *Ei*
- **Kaubakood:** *Kokku*
- **Ajalise jaotuse periood:** määrake see väli, et luua igakuiseid ajavahemikke.

Sellisel juhul sarnaneb loodud aruande sisu järgmise näitega.

<table>
<thead>
<tr>
    <th rowspan="2">Kaubakood</th>
    <th rowspan="2">Koht</th>
    <th rowspan="2">Laos olev kogus</th>
    <th rowspan="2">Laoseisu väärtus</th>
    <th rowspan="2">Laoväärtuse kogus</th>
    <th rowspan="2">Laoväärtus</th>
    <th rowspan="2">Keskmine ühikukulu</th>
    <th colspan="2">01.05.2020–08.05.2020</th>
    <th colspan="2">01.04.2020–30.04.2020</th>
    <th colspan="2">01.03.2020–31.03.2020</th>
</tr>
<tr>
    <th>P1: kogus</th>
    <th>P1: summa</th>
    <th>P2: kogus</th>
    <th>P2: summa</th>
    <th>P3: kogus</th>
    <th>P3: summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1283,33</td>
    <td>14</td>
    <td>1283,33</td>
    <td>91,67</td>
    <td></td>
    <td></td>
    <td>5,00</td>
    <td>458,33</td>
    <td>9,00</td>
    <td>825,00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2000,00</td>
    <td>10</td>
    <td>2000,00</td>
    <td>200,00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2000,00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 kokku</strong></td>
    <td></td>
    <td><strong>24,00</strong></td>
    <td><strong>3283,33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5,00</strong></td>
    <td><strong>458,33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2825,00</strong></td>
</tr>
</tfoot>
</table>

Pöörake selles näidisaruandes tähelepanu järgmistele üksikasjadele.

- Aruandes toodud väärtused **Laoväärtuse kogus**, **Laoväärtus** ja **Keskmine ühikukulu** on finantsilise varude dimensiooni (praegusel juhul **Koht**) väärtused.

    Näiteks kuvatakse koha 1 puhul aruandes järgmine teave.

    - **Laoväärtuse koguse** väärtus on *14* (= 10 + 5 – 5 + 5 – 1).
    - **Laoväärtuse** väärtus on *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).
    - **Keskmine ühikukulu** on *91,67*.
    - Igas perioodis arvutatakse väärtused **Laoseisu väärtus** ja **Summa** väärtuse **Keskmine ühikukulu** alusel.

- Aruandes määratletakse iga perioodi laos olev kogus sellel perioodil vastuvõetud varude koguste kokkuliitmise kaudu. Seejärel rakendatakse kogu väljastatud koguse lahutamiseks esimesena sisse, esimesena välja (FIFO) põhimõtet, sõltumata laomudelist, mida kaubad kasutavad.

Kui käivitate sama aruande uuesti, kuid määrate seekord väljade **Koht** ja **Ladu** väärtuseks *Kuva*, sarnaneb uus aruanne järgmise näitega.

<table>
<thead>
<tr>
    <th rowspan="2">Kaubakood</th>
    <th rowspan="2">Koht</th>
    <th rowspan="2">Ladu</th>
    <th rowspan="2">Laos olev kogus</th>
    <th rowspan="2">Laoseisu väärtus</th>
    <th rowspan="2">Laoväärtuse kogus</th>
    <th rowspan="2">Laoväärtus</th>
    <th rowspan="2">Keskmine ühikukulu</th>
    <th colspan="2">01.05.2020–08.05.2020</th>
    <th colspan="2">01.04.2020–30.04.2020</th>
    <th colspan="2">01.03.2020–31.03.2020</th>
</tr>
<tr>
    <th>P1: kogus</th>
    <th>P1: summa</th>
    <th>P2: kogus</th>
    <th>P2: summa</th>
    <th>P3: kogus</th>
    <th>P3: summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916,67</td>
    <td>14</td>
    <td>1283,33</td>
    <td>91,67</td>
    <td></td>
    <td></td>
    <td>5,00</td>
    <td>458,33</td>
    <td>5,00</td>
    <td>458,33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366,67</td>
    <td>14</td>
    <td>1283,33</td>
    <td>91,67</td>
    <td>4,00</td>
    <td>366,67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2000,00</td>
    <td>10</td>
    <td>2000,00</td>
    <td>200,00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2000,00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 kokku</strong></td>
    <td></td>
    <td></td>
    <td><strong>24,00</strong></td>
    <td><strong>3283,33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4,00</strong></td>
    <td><strong>366,67</strong></td>
    <td><strong>5,00</strong></td>
    <td><strong>458,33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2458,33</strong></td>
</tr>
</tfoot>
</table>

Seekord on koht 1 jagatud kaheks reaks: üks lao 11 ja üks lao 12 jaoks. Kuid väärtused **Laoväärtuse kogus**, **Laoväärtus** ja **Keskmine ühikukulu** on samad, kuna **Ladu** pole finantsiline varude dimensioon.

Lisaks pange tähele, et koha 1 koguse jaotus on erinev. Esimeses käivitatud aruandes eiras süsteem samas kohas toimunud üleviimistellimust ja lahutas müügiarve koguse koha 1 perioodist **01.03.2020–31.03.2020**. Kuid uues aruandes lahutab süsteem müügiarve koguse lao 12 perioodist **01.05.2020–08.05.2020**.

## <a name="effects-of-inventory-closing"></a>Lao sulgemise mõju

Kui käivitate lao sulgemise maikuu jaoks ja käivitate seejärel eelmise aruande uuesti, kuid seadistate välja **Kuupäevaga** väärtuseks *31. mai 2020*, peaksite märkama järgmisi tulemusi.

- Väärtused **Laoväärtus** ja **Keskmine ühikukulu** on uuendatud.
- Iga perioodi puhul on väärtused **Laoseisu väärtus** ja **Summa** samuti vastavalt uuendatud.

Uus aruanne sarnaneb järgmise näitega.

<table>
<thead>
<tr>
    <th rowspan="2">Kaubakood</th>
    <th rowspan="2">Koht</th>
    <th rowspan="2">Ladu</th>
    <th rowspan="2">Laos olev kogus</th>
    <th rowspan="2">Laoseisu väärtus</th>
    <th rowspan="2">Laoväärtuse kogus</th>
    <th rowspan="2">Laoväärtus</th>
    <th rowspan="2">Keskmine ühikukulu</th>
    <th colspan="2">01.05.2020–31.05.2020</th>
    <th colspan="2">01.04.2020–30.04.2020</th>
    <th colspan="2">01.03.2020–31.03.2020</th>
</tr>
<tr>
    <th>P1: kogus</th>
    <th>P1: summa</th>
    <th>P2: kogus</th>
    <th>P2: summa</th>
    <th>P3: kogus</th>
    <th>P3: summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910,70</td>
    <td>14</td>
    <td>1275,00</td>
    <td>91,07</td>
    <td>0,00</td>
    <td></td>
    <td>5,00</td>
    <td>455,36</td>
    <td>5,00</td>
    <td>455,36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364,29</td>
    <td>14</td>
    <td>1275,00</td>
    <td>91,07</td>
    <td>4,00</td>
    <td>364,29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2000,00</td>
    <td>10</td>
    <td>2000,00</td>
    <td>200,00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2000,00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 kokku</strong></td>
    <td></td>
    <td></td>
    <td><strong>24,00</strong></td>
    <td><strong>3275,00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4,00</strong></td>
    <td><strong>364,29</strong></td>
    <td><strong>5,00</strong></td>
    <td><strong>455,36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2455,36</strong></td>
</tr>
</tfoot>
</table>
