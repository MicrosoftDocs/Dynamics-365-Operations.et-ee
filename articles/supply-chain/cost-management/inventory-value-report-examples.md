---
title: Varude väärtuse aruande näited ja loogika
description: See artikkel annab mõned näited tulemustest, mis on esitatud iga laoväärtuse aruande tüübi puhul. Laoväärtuse aruanded annavad üksikasju teie varude füüsiliste ja finantskoguste ja -summade kohta.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e6c6387be5204fde6ebc7a4983567801900974af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877649"
---
# <a name="inventory-value-report-examples-and-logic"></a>Varude väärtuse aruande näited ja loogika

[!include [banner](../includes/banner.md)]

Laoväärtuse aruanded annavad üksikasju teie varude füüsiliste ja finantskoguste ja -summade kohta. See artikkel annab mõned näited tulemustest, mis on esitatud iga laoväärtuse aruande tüübi puhul.

Lisateavet iga laoväärtuse aruande tüübi loomise ja kasutamise kohta vt laoväärtuse [aruannetest](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Näidetes kasutatavad näidisandmed

Selle artikli näited põhinevad selles jaotises kirjeldatud laokannete näidisandmetel.

### <a name="storage-dimension-setup"></a>Laoala dimensiooni seadistamine

Näidissüsteemis on laoala dimensioonid sätestatud järgmiselt.

| Nimi | Aktiivne | Füüsiline ladu | Finantsiline laovaru |
|---|---|---|---|
| Koht | Jah | Jah | Jah |
| Ladu | Jah | Jah | Ei |

### <a name="inventory-model"></a>Laomudel

Näiteks on väljastatud toodete laomudel *FIFO* **·** *ja laomudeli omahinna välja väärtuseks on seatud Kaasa füüsiline väärtus*.

### <a name="inventory-transactions"></a>Laokanded

Näitesüsteem sisaldab järgmisi väljastatud toote laokandeid kaubakoodiga *B0001*.

| Viide | Sait | Ladu | Sissetulek | Probleem | Füüsiline kuupäev | Finantskuupäev | Kogus | Sisseostuhind | Füüsiline omahind |
|---|---|---|---|---|---|---|---|---|---|
| Ostutellimus | 1 | 11 | Ostetud | | 15. märts | 15. märts | 10 | 1000 | 1000 |
| Ostutellimus | 2 | 21 | Ostetud | | 15. märts | 15. märts | 10 | 2,000 | 2,000 |
| Ostutellimus | 1 | 11 | Vastuvõetud | | 15. aprill | | 5 | | 375 |
| Üleviimistellimus | 1 | 11 | | Müüdud | 2. mai | 2. mai | -5 | -458,33 | -458,33 |
| Üleviimistellimus | 1 | 12 | Ostetud | | 2. mai | 2. mai | 5 | 458.33 | 458.33 |
| Müügitellimus | 1 | 12 | | Müüdud | 3. mai | 3. mai | –1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Laoväärtuse aruande konfiguratsioon

Näiteks süsteem hõlmab varude väärtuse aruande konfiguratsiooni, milles on järgmised sätted:

- **Vahemik:** *sisestuskuupäev*
- **Varud:** *jah*
- **Keskmise ühikukulu arvutamine:** *jah*
- **Kogus kokku ja väärtus:** *Jah*
- **Sait, vaade:** *valitud*
- **Ressursi ID, kuva:** *jah*
- **Tase:** *kogusummad*

## <a name="inventory-value-report-example-1"></a>Laoväärtuse aruande näide 1

Järgmine tabel ja illustratsioonid näitavad tulemusi, kui kasutate näidisandmeid ja aruande konfiguratsiooni, mida kirjeldatakse selles artiklis varem.

| Ressursi tüüp | Ressurss | Sait | Viide | Varud: rahaline kogus | Varud: rahaline summa | Varud: füüsiline kogus on sisestatud. | Varud: füüsiline summa on sisestatud. | Varud: kogus | Varud: summa | Keskmine ühikukulu |
|---|---|---|---|---|---|---|---|---|---|---|
| Materjal | B0001 (üks) | 1 | Ending balance | 9,00 | 908.33 | 5.00 | 375.00 | 14.00 | 1283,33 | 91,67 |
| Materjal | B0001 (üks) | 2 | Ending balance | 10.00 | 2000,00 | 0.00 | 0.00 | 10.00 | 2000,00 | 200,00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standardne laoväärtuse aruanne, näiteks 1

Järgmine näide näitab standardset varude **väärtuse** aruannet, nt 1. (Valige illustratsioon, et avada suurem versioon.)

[![Laoväärtuse aruanne näiteks 1.](media/inventory-value-report-ex1-small.png "Laoväärtuse aruanne, näiteks 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Laoväärtuse aruande ladustamisaruanne, näiteks 1

Järgmine joonis näitab varude väärtuse **aruande ladustamisaruannet**, nt 1. (Valige illustratsioon, et avada suurem versioon.)

[![Laoväärtuse aruande ladustamisaruanne, näiteks 1.](media/inventory-value-report-storage-ex1-small.png "Laoväärtuse aruande ladustamisaruanne, näiteks 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Laoväärtuse aruande näide 2

Järgmine tabel ja illustratsioonid näitavad tulemusi, **·** *kui kasutate näidisandmeid, mida kirjeldatakse selles artiklis,* aga te muudate välja **Tase** *väärtuse aruande konfiguratsioonis kanneteks ja määrate välja Alates kuupäevast väärtuseks 15*, kui käivitate aruande.

| Ressursi tüüp | Ressurss | Sait | Kuupäev | Number | Viide | Varud: rahaline kogus | Varud: rahaline summa | Varud: füüsiline kogus on sisestatud. | Varud: füüsiline summa on sisestatud. | Varud: kogus | Varud: summa |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materjal | B0001 (üks) | 1 | 3/15/2021 | 00000126 | Ostutellimus | 0.00 | 0.00 | 10.00 | 1,000.00 | **10.00** | **1,000.00** |
| Materjal | B0001 (üks) | 1 | 3/15/2021 | 00000126 | Ostutellimus | 10.00 | 1,000.00 | -10,00 | –1000,00 | **0.00** | **0.00** |
| Materjal | B0001 (üks) | 1 | 4/15/2021 | 00000128 | Ostutellimus | 0.00 | 0.00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Materjal | B0001 (üks) | 1 | 5/2/2021 | 000003 | Üleviimistellimuse saadetis | –5,00 | -458,33 | 0.00 | 0.00 | **-5.00** | **-458.33** |
| Materjal | B0001 (üks) | 1 | 5/2/2021 | 000003 | Üleviimistellimuse tarne | 5.00 | 458.33 | 0.00 | 0.00 | **5.00** | **458.33** |
| Materjal | B0001 (üks) | 1 | 5/3/2021 | 000835 | Müügitellimus | 0.00 | 0.00 | –1,00 | -91,67 | **-1.00** | **-91.67** |
| Materjal | B0001 (üks) | 1 | 5/3/2021 | 000835 | Müügitellimus | –1,00 | -91,67 | 1.00 | 91,67 | **0.00** | **0.00** |
| Materjal | B0001 (üks) | 2 | 3/15/2021 | 00000127 | Ostutellimus | 0.00 | 0.00 | 10.00 | 2000,00 | **10.00** | **2,000.00** |
| Materjal | B0001 (üks) | 2 | 3/15/2021 | 00000127 | Ostutellimus | 10.00 | 2000,00 | -10,00 | ‑2000,00 | **0.00** | **0.00** |
| Materjal | B0001 (üks) | 2 | 5/2/2021 | 000003 | Üleviimistellimuse saadetis | 5.00 | 458.33 | 0.00 | 0.00 | **5.00** | **458.33** |
| Materjal | B0001 (üks) | 2 | 5/2/2021 | 000003 | Üleviimistellimuse tarne | –5,00 | -458,33 | 0.00 | 0.00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Standardne laoväärtuse aruanne, näiteks 2

Järgmine näide näitab laoväärtuse standardaruannet **2**. (Valige illustratsioon, et avada suurem versioon.)

[![Laoväärtuse aruanne, näiteks 2.](media/inventory-value-report-ex2-small.png "Laoväärtuse aruanne, näiteks 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Laoväärtuse aruande ladustamisaruanne, näiteks 2

Järgmine joonis näitab varude väärtuse **aruande ladustamisaruannet**, nt 2. (Valige illustratsioon, et avada suurem versioon.)

[![Laoväärtuse aruande ladustamisaruanne, näiteks 2.](media/inventory-value-report-storage-ex2-small.png "Laoväärtuse aruande ladustamisaruanne, näiteks 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Laoväärtuse aruande näide 3

Soovitame teil käivitada laoväärtuse aruanded pärast ümberarvutamist või lao sulgemist, et teil oleks kanded ja summad, mida ümberarvutamine või lao sulgemine mõjutab.

Järgmised alamjaotised näitavad laoväärtuse aruandeid, mis luuakse pärast lao sulgemist kuni 30. maini.

### <a name="example-3-when-the-totals-level-is-used"></a>Näide 3, kui kasutatakse taseme Kogusummad

Järgmine tabel näitab tulemusi, kui kasutate näidisandmeid ja aruande konfiguratsiooni, mida kirjeldatakse selles artiklis varem. (Selles aruande konfiguratsioonis **Taseme** välja väärtuseks on seatud *Kogusummad*.)

| Ressursi tüüp | Ressurss | Sait | Viide | Varud: rahaline kogus | Varud: rahaline summa | Varud: füüsiline kogus on sisestatud. | Varud: füüsiline summa on sisestatud. | Varud: kogus | Varud: summa | Keskmine ühikukulu |
|---|---|---|---|---|---|---|---|---|---|---|
| Materjal | B0001 (üks) | 1 | Ending balance | 9,00 | 900.00 | 5.00 | 375.00 | 14.00 | 1275,00 | 91,07 |
| Materjal | B0001 (üks) | 2 | Ending balance | 10.00 | 2000,00 | 0.00 | 0.00 | 10.00 | 2000,00 | 200,00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Näide 3, kui kasutatakse kannete taset

Järgmine tabel näitab tulemusi, kui kasutate näidisandmeid, mida kirjeldatakse selles artiklis varem, **kuid te muudate välja Tase** *väärtuse* aruande konfiguratsioonis kanneteks.

| Ressursi tüüp | Ressurss | Sait | Kuupäev | Number | Viide | Varud: rahaline kogus | Varud: rahaline summa | Varud: füüsiline kogus on sisestatud. | Varud: füüsiline summa on sisestatud. | Varud: kogus | Varud: summa |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materjal | B0001 (üks) | 1 | 3/15/2021 | 00000126 | Ostutellimus | 0.00 | 0.00 | 10.00 | 1,000.00 | 10.00 | 1,000.00 |
| Materjal | B0001 (üks) | 1 | 3/15/2021 | 00000126 | Ostutellimus | 10.00 | 1,000.00 | -10,00 | –1000,00 | 0.00 | 0.00 |
| Materjal | B0001 (üks) | 1 | 4/15/2021 | 00000128 | Ostutellimus | 0.00 | 0.00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Materjal | B0001 (üks) | 1 | 5/2/2021 | 000003 | Üleviimistellimuse saadetis | –5,00 | -458,33 | 0.00 | 0.00 | –5,00 | -458,33 |
| Materjal | B0001 (üks) | 1 | 5/2/2021 | 000003 | Üleviimistellimuse tarne | 5.00 | 458.33 | 0.00 | 0.00 | 5.00 | 458.33 |
| Materjal | B0001 (üks) | 1 | 5/3/2021 | 000835 | Müügitellimus | 0.00 | 0.00 | –1,00 | -91,67 | –1,00 | -91,67 |
| Materjal | B0001 (üks) | 1 | 5/3/2021 | 000835 | Müügitellimus | –1,00 | -91,67 | 1.00 | 91,67 | 0.00 | 0.00 |
| Materjal | B0001 (üks) | 1 | 5/31/2021 | 000835 | Müügitellimus | 0.00 | -8.33 | 0.00 | 0.00 | 0.00 | -8.33 |
| Materjal | B0001 (üks) | 1 | 5/31/2021 | 000003 | Üleviimistellimuse saadetis | 0.00 | -41.67 | 0.00 | 0.00 | 0.00 | -41.67 |
| Materjal | B0001 (üks) | 1 | 5/31/2021 | 000003 | Üleviimistellimuse tarne | 0.00 | 41.67 | 0.00 | 0.00 | 0.00 | 41.67 |
| Materjal | B0001 (üks) | 2 | 3/15/2021 | 00000127 | Ostutellimus | 0.00 | 0.00 | 10.00 | 2000,00 | 10.00 | 2000,00 |
| Materjal | B0001 (üks) | 2 | 3/15/2021 | 00000127 | Ostutellimus | 10.00 | 2000,00 | -10,00 | ‑2000,00 | 0.00 | 0.00 |
| Materjal | B0001 (üks) | 2 | 5/2/2021 | 000003 | Üleviimistellimuse saadetis | 5.00 | 458.33 | 0.00 | 0.00 | 5.00 | 458.33 |
| Materjal | B0001 (üks) | 2 | 5/2/2021 | 000003 | Üleviimistellimuse tarne | –5,00 | -458,33 | 0.00 | 0.00 | –5,00 | -458,33 |
| Materjal | B0001 (üks) | 2 | 5/31/2021 | 000003 | Üleviimistellimuse saadetis | 0.00 | 41.67 | 0.00 | 0.00 | 0.00 | 41.67 |
| Materjal | B0001 (üks) | 2 | 5/31/2021 | 000003 | Üleviimistellimuse tarne | 0.00 | -41.67 | 0.00 | 0.00 | 0.00 | -41.67 |
