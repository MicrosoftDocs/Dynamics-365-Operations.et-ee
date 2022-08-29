---
title: ER-i funktsioon POWER
description: See artikkel annab teavet POWER-elektroonilise aruandluse (ER) funktsiooni kohta.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273990"
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
