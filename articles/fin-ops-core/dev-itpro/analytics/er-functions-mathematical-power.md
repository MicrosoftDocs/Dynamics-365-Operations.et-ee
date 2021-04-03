---
title: ER-i funktsioon POWER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni POWER.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9c45e7f9b47a3f0ff4445b1dd160def0ada3a56e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570418"
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