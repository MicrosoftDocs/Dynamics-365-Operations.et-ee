---
title: ER-i funktsioon INTVALUE
description: See artikkel annab teavet selle kohta, kuidas kasutatakse intVALUE elektroonilise aruandluse (ER) funktsiooni.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282617"
---
# <a name="intvalue-er-function"></a>ER-i funktsioon INTVALUE

[!include [banner](../includes/banner.md)]

Funktsioon `INTVALUE` tagastab väärtuse *Int*, mis tähistab määratud stringi.

## <a name="syntax-1"></a>Süntaks 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Teksti väärtus, mis tuleb teisendada numbriks *Int*.

`number`: *tegelik* või *täisarv*

Numbriline *tegelik* või *täisarvuline* väärtus, mis tuleb teisendada numbriks *Int*.

## <a name="return-values"></a>Tagastusväärtused

*Int*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kümnendkohad kärbitakse.

## <a name="example-1"></a>Näide 1

`INTVALUE ("100.77")` tagastab *Int* väärtuse **100**.

## <a name="example-2"></a>Näide 2

`INTVALUE (-100.77)` tagastab *Int* väärtuse **–100**.

## <a name="additional-resources"></a>Lisaressursid

[Tüübiteisenduse funktsioonid](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
