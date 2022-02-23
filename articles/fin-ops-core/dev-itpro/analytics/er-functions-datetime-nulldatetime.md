---
title: ER-i funktsioon NULLDATETIME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NULLDATETIME.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 65e9ef92dc30e46c297d93e262bad8878df47a0c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682289"
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
