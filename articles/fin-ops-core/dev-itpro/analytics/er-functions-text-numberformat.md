---
title: ER-i funktsioon NUMBERFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMBERFORMAT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a431414044846bf4e79e6b9f0e5b27281ea8f46
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744403"
---
# <a name="numberformat-er-function"></a>ER-i funktsioon NUMBERFORMAT

[!include [banner](../includes/banner.md)]

Funktsioon `NUMBERFORMAT` tagastab *stringi* väärtuse, mis esitab määratud numbri määratud vormingus ja valikuliselt määratletud [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

## <a name="syntax-1"></a>Süntaks 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumendid

`number`: *täisarv* või *tegelik*

Numbriline väärtus, mis määrab arvu, mis tuleb välja vormindada.

`format`: *string*

*Stringi* väärtus, mis tähistab vormingut.

`culture`: *string*

*Stringi* väärtus, mis tähistab vormindamiseks kasutatavat kultuuri.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui kultuuri ei määratleta kutsutava funktsiooni argumendina, määratleb kontekst, mida selle funktsiooni käitamiseks kasutatakse, numbrite vormindamiseks kasutatava kultuuri.

## <a name="example-1"></a>Näide 1

Kultuuris **EN-US** `NUMBERFORMAT (0.45, "p")` tagastab **„45.00 %”** ja `NUMBERFORMAT (10.45, "#")` tagastab **„10”**.

## <a name="example-2"></a>Näide 2

`NUMBERFORMAT (10/3, "F2", "de")` tagastab **3,33**, samas kui `NUMBERFORMAT (10/3, "F2", "en-us")` tagastab **3.33**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)
