---
title: ER-i funktsioonide loend tüübiteisenduse kategoorias
description: See teema annab teavet teisendamise funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d160c02403bf067ed523fbd634e65c622b522b97
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686070"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>ER-i funktsioonide loend tüübiteisenduse kategoorias

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) tüübiteisenduse funktsioone saab kasutada väärtuste teisendamiseks tüüpide vahel. See teema sisaldab järgmiste funktsioonide kokkuvõtet.

## <a name="type-conversion-functions"></a>Tüübiteisenduse funktsioonid

| Funktsioon | Kirjeldus |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | See funktsioon tagastab väärtuse *Int64*, mis tähistab määratud stringi. |
| [IntValue](er-functions-conversion-intvalue.md)       | See funktsioon tagastab väärtuse *Int*, mis tähistab määratud stringi. |
| [NumberValue](er-functions-conversion-numbervalue.md) | See funktsioon tagastab *tegeliku* väärtuse, mis konverteeritakse määratud *stringi* väärtusest. Teisendamise käigus arvestatakse määratud kümnendkoha ja arvu rühmitamise eraldajaga. |
| [Väärtus](er-functions-conversion-value.md)             | See funktsioon tagastab *tegeliku* väärtuse, mis konverteeritakse määratud *stringi* väärtusest. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Tüübiteisenduse funktsioonid kuupäeva ja kellaaja kategoorias

Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [kuupäeva ja kellaaja kategoorias](er-functions-category-datetime.md).

| Funktsioon | Kirjeldus |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis on antud *stringi* väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva/kellaaja väärtuse kultuuris. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis teisendatakse määratud *kuupäeva* väärtusest kuupäeva/kellaaja väärtuseks koordineeritud maailmaajas (Greenwichi aeg \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | See funktsioon tagastab *kuupäeva* väärtuse, mis on antud *stringi* väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva väärtuse kultuuris. |

## <a name="type-conversion-functions-in-the-list-category"></a>Tüübiteisenduse funktsioonid loendi kategoorias

Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [loendi kategoorias](er-functions-category-list.md).

| Funktsioon | Kirjeldus |
|----------|-------------|
| [Loend](er-functions-list-list.md)                 | See funktsioon tagastab *kirjete loendi* väärtuse uue loendina, mis on loodud *konteineri (kirje)* määratud argumentidest. |
| [ListOfFields](er-functions-list-listoffields.md) | See funktsioon tagastab *kirjete loendi* väärtuse, mis luuakse tüübi *Loetelu* või *Konteiner (kirje)* antud argumendi struktuuri põhjal. |
| [Tükeldamine](er-functions-list-split.md)               | See funktsioon tükeldab määratud *stringi* väärtuse alamstringideks ja tagastab tulemuse uue *kirjete loendi* väärtusena. |
| [StringJoin](er-functions-list-stringjoin.md)     | See funktsioon tagastab *stringi* väärtuse, mis koosneb määratud *kirjete loendi* väärtuse määratud välja liitväärtustest. Väärtused saab eraldada määratud eraldajaga. |

## <a name="type-conversion-functions-in-the-text-category"></a>Tüübiteisenduse funktsioonid teksti kategoorias

Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [teksti kategoorias](er-functions-category-text.md).

| Funktsioon | Kirjeldus |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | See funktsioon tagastab *stringi* väärtuse, mis esindab üksikut märki, millele viitab määratud Unicode’i number. |
| [GuidValue](er-functions-text-guidvalue.md)       | See funktsioon teisendab *stringi* tüübi määratud sisendi andmeüksuseks tüübiga *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | See funktsioon tagastab *stringi* väärtuse, mis esindab määratud numbrit määratud vormingus ja valikuliselt määratletud kultuuris. |
| [QrCode](er-functions-text-qrcode.md)             | See funktsioon tagastab *konteineri* väärtuse, mis esitab määratud stringi puhul binaarvormingus ruutkoodi (QR-koodi) pildi. |
| [Tekst](er-functions-text-text.md)                 | See funktsioon tagastab *stringi* väärtuse, mis esindab määratud numbrit pärast seda, kui see on teisendatud tekstistringiks, mis on vormindatud praeguse rakenduse eksemplari serverilokaadi sätete kohaselt. |

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse valemi keel](er-formula-language.md)
