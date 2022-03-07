---
title: ER-i funktsioon INTVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni INTVALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755368"
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