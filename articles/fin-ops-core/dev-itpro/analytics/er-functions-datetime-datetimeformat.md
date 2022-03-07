---
title: ER-i funktsioon DATETIMEFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATETIMEFORMAT.
author: NickSelin
ms.date: 09/08/2021
ms.prod: ''
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
ms.openlocfilehash: 1add2ccb348a9b518e0121be1184fbf6a684a0df
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485542"
---
# <a name="datetimeformat-er-function"></a>ER-i funktsioon DATETIMEFORMAT

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` Funktsioon tagastab *[Stringi](er-formula-supported-data-types-primitive.md#string)* väärtuse, mis esitab antud kuupäeva/kellaaja väärtuse määratud vormingus tekstina ja valikuliselt määratletud [kultuuris](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Süntaks 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Argumendid

`datetime`: *[KuupäevKellaaeg](er-formula-supported-data-types-primitive.md#datetime)*

Kuupäeva/kellaaja väärtus, mis tähistab vormindatavat kuupäeva ja kellaaega.

`format`: *string*

Väljundstringi vorming. Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> Vormingu string on tõstutundlik, kui kasutate kas standardvormingut või kohandatud vormingut. Näiteks [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) vormingu määraja „d” tagastab kuupäeva, kasutades lühikest kuupäeva mustrit, samas kui standardne vormingu määraja „D” tagastab kuupäeva pikka kuupäeva mustrit kasutades. Lisaks tagastab [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings) vormingu määraja „M” kuu vahemikus 1 kuni 12, samas kui kohandatud vormingu määraja „m” tagastab minuti vahemikus 0 kuni 59.

`culture`: *string*

Vormindamiseks kasutatav kultuur. Lisateabe saamiseks toetatud kultuuride kohta vaata [kultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud stringi väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst. Näiteks kui funktsioon `DATETIMEFORMAT` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades. Olemi `culture` vaikeväärtus on **EN-US**.

Kui funktsioon `DATETIMEFORMAT` teisendab antud kuupäeva/kellaaja väärtuse, siis see arvestab rakenduse kasutaja ajavööndit, kes käitab ER-vormingut, mille kontekstis funktsiooni kutsutakse.

## <a name="example-1"></a>Näide 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` annab vastuseks praeguse rakendusserveri kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24-12-2015”** määratud kohandatud vormingu kohaselt.

## <a name="example-2"></a>Näide 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24.12.2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.

## <a name="example-3"></a>Näide 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` tagastab stringi väärtuse **2019-11-12T08:00:00.0000000-08:00**, kui see funktsioon kutsutakse toimigu ajal, mis käivitati rakenduse kasutaja poolt, kelle ajavööndi väärtus on **(GMT-08:00) Vaikse ookeani aeg (Ameerika Ühendriigid ja Kanada)** jaotises **Keele ja riigi/regiooni eelistused**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
