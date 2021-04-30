---
title: ER-i funktsioon DATEFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATEFORMAT.
author: NickSelin
ms.date: 01/04/2021
ms.topic: article
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
ms.openlocfilehash: 1b3a0a2608328b233004034f7ab2ccfa833c17e3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890906"
---
# <a name="dateformat-er-function"></a>ER-i funktsioon DATEFORMAT

[!include [banner](../includes/banner.md)]

Funktsioon `DATEFORMAT` tagastab *stringi* väärtuse, mis esitab antud kuupäeva väärtuse määratud vormingus tekstina ja valikuliselt määratletud [kultuuris](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Süntaks 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumendid

`date`: *kuupäev*

Kuupäeva väärtus, mis tähistab vormindatavat kuupäeva.

`format`: *string*

Väljundstringi vorming.

> [!NOTE]
> Vormingu string on tõstutundlik, kui kasutate kas standardvormingut või kohandatud vormingut. Näiteks [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) vormingu määraja „d” tagastab kuupäeva, kasutades lühikest kuupäeva mustrit, samas kui standardne vormingu määraja „D” tagastab kuupäeva pikka kuupäeva mustrit kasutades. Lisaks tagastab [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings) vormingu määraja „M” kuu vahemikus 1 kuni 12, samas kui kohandatud vormingu määraja „m” tagastab minuti vahemikus 0 kuni 59.

`culture`: *string*

Vormindamiseks kasutatav kultuur.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud stringi väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst. Näiteks kui funktsioon `DATEFORMAT` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades. Olemi `culture` vaikeväärtus on **EN-US**.

## <a name="example-1"></a>Näide 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` tagastab praeguse rakendusserveri kuupäeva väärtuse 24. detsember 2015 stringi kujul **„24-12-2015”** määratud kohandatud vormingu kohaselt.

## <a name="example-2"></a>Näide 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva 24. detsember 2015 stringina **„24-12-2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]