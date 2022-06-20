---
title: ER-i funktsioon NULLDATETIME
description: See artikkel annab teavet selle kohta, kuidas nulldatetime elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 3e8447d4f05ee8394842b9b07d14d1c054834bb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867668"
---
# <a name="nulldatetime-er-function"></a>ER-i funktsioon NULLDATETIME

[!include [banner](../includes/banner.md)]

Funktsioon `NULLDATETIME` tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuar 1900) koordineeritud maailmaajas (Greenwichi aeg \[GMT\]).

## <a name="syntax"></a>Süntaks

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Tagastusväärtused

*DateTime*

Tulemiks saadud kuupäeva/kellaaja väärtus.

## <a name="example"></a>Näide

`DATETIMEFORMAT( NULLDATETIME(), "O")` tagastab stringi väärtuse **1900-01-01T00:00:00.0000000+00:00**, kui see kutsutakse toimigu ajal, mis käivitati rakenduse kasutaja poolt, kelle ajavööndi väärtus on **(GMT) koordineeritud maailmaaeg** jaotises **Keele ja riigi/regiooni eelistused**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]