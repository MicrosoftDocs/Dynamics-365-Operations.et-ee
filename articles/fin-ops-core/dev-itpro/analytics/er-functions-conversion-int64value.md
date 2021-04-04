---
title: ER-i funktsioon INT64VALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni INT64VALUE.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 9db2e9abcac36a8331a494c886218bbfc82e93aa
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561490"
---
# <a name="int64value-er-function"></a>ER-i funktsioon INT64VALUE

[!include [banner](../includes/banner.md)]

Funktsioon `INT64VALUE` tagastab väärtuse *Int64*, mis tähistab määratud stringi.

## <a name="syntax-1"></a>Süntaks 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Teksti väärtus, mis tuleb teisendada numbriks *Int64*.

`number`: *tegelik* või *täisarv*

Numbriline *tegelik* või *täisarvuline* väärtus, mis tuleb teisendada numbriks *Int64*.

## <a name="return-values"></a>Tagastusväärtused

*Int64*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kümnendkohad kärbitakse.

## <a name="example-1"></a>Näide 1

`INT64VALUE ("22565422744")` tagastab *Int64* väärtuse **22565422744**.

## <a name="example-2"></a>Näide 2

`INT64VALUE ( VALUE("22565422744.77"))` tagastab *Int64* väärtuse **22565422744**.

## <a name="additional-resources"></a>Lisaressursid

[Tüübiteisenduse funktsioonid](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]