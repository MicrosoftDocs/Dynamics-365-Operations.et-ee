---
title: Sissetulevate dokumentide sõelumine JSON-vormingus
description: See artikkel selgitab, kuidas seadistada elektroonilise aruandluse (ER) vorminguid sissetulevate dokumentide sõelumiseks JavaScripti objekti notationi (JSON) vormingus.
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 93a2f669a555beefc3a1529af4df7b543aaab931
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905076"
---
# <a name="parse-incoming-documents-in-json-format"></a>Sissetulevate dokumentide sõelumine JSON-vormingus

[!include[banner](../includes/banner.md)]

Saate kujundada elektroonilise aruandluse vormingud sõeluma sissetulevaid elektroonilisi dokumente, mis esitavad andmeid JavaScriptil põhinevas tekstivormingus (teisisõnu failid vormingus JavaScript Object Notation \[JSON\]).

Selle funktsiooni kohta lisateabe saamiseks laadige alla järgmises tabelis olevad failid ja seejärel esitage elektroonilise aruandluse vormingu konfiguratsiooni loomise importimiseks välisest JSON-failist tegevuse juhised. Selles tegevuse juhises näidatakse, kuidas elektroonilise aruandluse vormingut saab kasutada sissetuleva JSON-faili sõelumiseks rakenduse andmete värskendamiseks.

| Tiitel                                  | Faili nimi |
|----------------------------------------|-----------|
| Elektroonilise aruandluse vormingu konfiguratsioon                | [Hankija kannete importimise vorming_JSON.xml](https://go.microsoft.com/fwlink/?linkid=874111) |
| CSV-vormingus sissetuleva faili näidis | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Nõuded

Enne elektroonilise aruandluse vormingu konfiguratsiooni loomise importimiseks välisest JSON-failist tegevuse juhiste lõpetamist peavad olema täidetud järgmised nõuded.

- JSON-faili ülem-elemendid võivad olla ainult objekti elemendid.
- Objekti pesastatud elemendid peaksid olema atribuudi elemendid, et luuakse kehtiv JSON-i struktuur.
- JSON-massiivid võivad olla ainult objekti atribuudi elementide pesastatud elemendid.
- JSON-massiivid võivad sisaldada ainult JSON-objekte. Need ei saa sisaldada otseseid stringi/numbrilisi väärtusi ega pesastatud massiive. Nende massiivide elemente sõelutakse järjekorras, nagu need on vormingus määratud. Iga JSON-objekti puhul kaalutakse kordsuse sätteid.

Lisaks peate läbima tegevuse juhise [Elektrooniline aruandlus. Nõutavate konfiguratsioonide loomine andmete importimiseks välisest failist](tasks/er-required-configurations-import-data.md), kui te pole seda veel läbinud. Tegevuse juhise lõpuleviimiseks laadige alla järgmine fail.

| Tiitel                  | Faili nimi |
|------------------------|-----------|
| Elektroonilise aruandluse mudeli konfiguratsioon | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]