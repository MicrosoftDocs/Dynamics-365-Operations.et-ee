---
title: ER-i funktsioon EMPTYRECORD
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni EMPTYRECORD Electronic Reporting (ER).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 6f339347187f145b90f14d56017097ff3d7712e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886816"
---
# <a name="emptyrecord-er-function"></a>ER-i funktsioon EMPTYRECORD

[!include [banner](../includes/banner.md)]

Funktsioon `EMPTYRECORD` tagastab *konteineri (kirje)* väärtuse null, millel on sama struktuur, kui määratud kirjete loendil või kirjel.

## <a name="syntax"></a>Süntaks

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend* või *konteiner (kirje)*

Tüübi *Kirjete loend* või *Konteiner (kirje)* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

> [!NOTE] 
> Nullkirje on kirje, mille kõikidel väljadel on tühi väärtus. Tühi väärtus on arvude puhul **0** (null), stringide puhul tühi string jne.

## <a name="example"></a>Näide

`EMPTYRECORD (SPLIT ("abc", 1))` tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon `SPLIT`. Lisateavet vt [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Lisaressursid

[Kirje funktsioonid](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]