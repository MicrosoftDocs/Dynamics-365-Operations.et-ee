---
title: ER-i funktsioon EMPTYRECORD
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni EMPTYRECORD Electronic Reporting (ER).
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5046a1cb43f12863ddbdf241e8ba72071d1016ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280151"
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
