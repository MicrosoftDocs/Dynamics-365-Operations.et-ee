---
title: ER-i funktsioon NUMBERFORMAT
description: See artikkel annab teavet selle kohta, kuidas KASUTATAKSE FUNKTSIOONI NUMBERFORMAT Electronic Reporting (ER).
author: kfend
ms.date: 12/10/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 5519f549c10ba5c02e249592d040582c3f8dc44f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274791"
---
# <a name="numberformat-er-function"></a>ER-i funktsioon NUMBERFORMAT

[!include [banner](../includes/banner.md)]

Funktsioon `NUMBERFORMAT` tagastab *stringi* väärtuse, mis esitab määratud numbri määratud vormingus ja valikuliselt määratletud [kultuuris](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-numeric-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-numeric-format-strings).

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
