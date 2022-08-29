---
title: ER-i funktsioon NOT
description: See artikkel annab teavet SELLE kohta, kuidas NOT Electronic Reporting (ER) funktsiooni kasutatakse.
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
ms.openlocfilehash: 032cdaa2c71f6fab8c15780594d5a26d73600e74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278972"
---
# <a name="not-er-function"></a>ER-i funktsioon NOT

[!include [banner](../includes/banner.md)]

Funktsioon `NOT` annab määratud tingimuse pööratud loogilise väärtuse *kahendmuutuja* väärtusena.

## <a name="syntax"></a>Süntaks

```vb
NOT (condition)
```

## <a name="arguments"></a>Argumendid

`condition`: *kahendmuutuja*

Kehtiv tingimuslik avaldis, mis tuleb ennistada.

## <a name="return-values"></a>Tagastusväärtused

*Kahendmuutuja*

Tulemiks saadud *kahendmuutuja* väärtus.

## <a name="example"></a>Näide

`NOT (TRUE)` tagastab väärtuse **FALSE**.

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
