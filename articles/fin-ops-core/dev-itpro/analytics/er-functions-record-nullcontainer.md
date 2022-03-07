---
title: ER-i funktsioon NULLCONTAINER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NULLCONTAINER.
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
ms.openlocfilehash: 13159d9d7c8d1871886beb3cb1938ca8b0097e0efb6f10a9d1b229c49b9ff947
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738572"
---
# <a name="nullcontainer-er-function"></a>ER-i funktsioon NULLCONTAINER

[!include [banner](../includes/banner.md)]

Funktsioon `NULLCONTAINER` tagastab *konteineri (kirje)* väärtuse null, millel on sama struktuur, kui määratud kirjete loendil või kirjel.

## <a name="syntax"></a>Süntaks

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend* või *konteiner (kirje)*

Tüübi *Kirjete loend* või *Konteiner (kirje)* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

> [!NOTE] 
> See funktsioon on aegunud. Kasutage selle asemel funktsiooni `EMPTYRECORD`. Lisateavet vt [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Näide

`NULLCONTAINER (SPLIT ("abc", 1))` tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon `SPLIT`. Lisateavet vt [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Lisaressursid

[Kirje funktsioonid](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]