---
title: ER-i funktsioon POWER
description: See artikkel annab teavet POWER-elektroonilise aruandluse (ER) funktsiooni kohta.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da3ae988b57cb5588de1e2fd8ee962b77b5534ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864684"
---
# <a name="power-er-function"></a>ER-i funktsioon POWER

[!include [banner](../includes/banner.md)]

Funktsioon `POWER` tagastab *tegeliku* väärtuse, mis kajastab määratud astmele määratud positiivse numbri tõstmise tulemi.

## <a name="syntax"></a>Süntaks

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumendid

`number`: *tegelik* või *täisarv*

Numbriline väärtus, mis tuleb tõsta määratud määratud astmele.

`power`: *tegelik* või *täisarv*

Arvuline väärtus, mis tähistab määratud astet.

## <a name="return-values"></a>Tagastusväärtused

*Tegelik*

Tulemiks saadud numbriline väärtus.

## <a name="example-1"></a>Näide 1

`POWER (10, 2)` tagastab **100**.

## <a name="example-2"></a>Näide 2

`POWER (4, 0.5)` tagastab **2**.

## <a name="additional-resources"></a>Lisaressursid

[Matemaatilised funktsioonid](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]