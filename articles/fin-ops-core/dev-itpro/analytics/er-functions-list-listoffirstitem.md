---
title: ER-i funktsioon LISTOFFIRSTITEM
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni LISTOFFIRSTITEM Electronic reporting (ER).
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
ms.openlocfilehash: f4715becfb158826a2b5678aac6a58c987433192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881155"
---
# <a name="listoffirstitem-er-function"></a>ER-i funktsioon LISTOFFIRSTITEM

[!include [banner](../includes/banner.md)]

Funktsioon `LISTOFFIRSTITEM` tagastab *kirjete loendi* väärtuse, mis koosneb ainult määratud loendi esimesest kirjest.

## <a name="syntax"></a>Süntaks

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="example"></a>Näide

Avaldis `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` tagastab tekstiväärtuse **„A”**.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]