---
title: ER-i funktsioon LISTOFFIRSTITEM
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni LISTOFFIRSTITEM Electronic reporting (ER).
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
ms.openlocfilehash: dede32c58ef8dc67028ea17b8a26189f62f73593
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275468"
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
