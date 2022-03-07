---
title: ER-i funktsioon STRINGJOIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni STRINGJOIN.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: ac21651e0f5b5a1579b9335bb7f3217370c4d5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745517"
---
# <a name="stringjoin-er-function"></a>ER-i funktsioon STRINGJOIN

[!include [banner](../includes/banner.md)]

Funktsioon `STRINGJOIN` tagastab *stringi* väärtuse, mis koosneb määratud loendi määratud välja liitväärtustest. Väärtused saab eraldada määratud eraldajaga.

## <a name="syntax"></a>Süntaks

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`field`: *väli*

Andmetüübi *String* välja kehtiv tee määratud loendis.

`delimiter`: *string*

Eraldaja, mida kasutatakse alamstringide eraldamiseks.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

Kui sisestate olemi `SPLIT("abc" , 1)` andmeallikana **DS**, tagastab avaldis `STRINGJOIN (DS, DS.Value, "-")` tulemuse **„a-b-c”**.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]