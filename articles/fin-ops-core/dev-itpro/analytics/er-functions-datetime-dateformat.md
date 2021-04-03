---
title: ER-i funktsioon DATEFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATEFORMAT.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0a9580b0ab9e472796375f498059ec0864a919ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563650"
---
# <a name="dateformat-er-function"></a>ER-i funktsioon DATEFORMAT

[!include [banner](../includes/banner.md)]

Funktsioon `DATEFORMAT` tagastab *stringi* väärtuse, mis esitab antud kuupäeva väärtuse määratud vormingus tekstina ja valikuliselt määratletud [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

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
> Vormingu string on tõstutundlik, kui kasutate kas standardvormingut või kohandatud vormingut. Näiteks [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) vormingu määraja „d” tagastab kuupäeva, kasutades lühikest kuupäeva mustrit, samas kui standardne vormingu määraja „D” tagastab kuupäeva pikka kuupäeva mustrit kasutades. Lisaks tagastab [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) vormingu määraja „M” kuu vahemikus 1 kuni 12, samas kui kohandatud vormingu määraja „m” tagastab minuti vahemikus 0 kuni 59.

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