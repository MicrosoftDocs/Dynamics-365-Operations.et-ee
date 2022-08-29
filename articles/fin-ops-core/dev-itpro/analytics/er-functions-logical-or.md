---
title: ER-i funktsioon OR
description: See artikkel annab teavet SELLE kohta, kuidas OR-elektroonilise aruandluse (ER) funktsiooni kasutatakse.
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
ms.openlocfilehash: 99b5ee37af1ea1a69985fb79b762b31561334fd6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268082"
---
# <a name="or-er-function"></a>ER-i funktsioon OR

[!include [banner](../includes/banner.md)]

Kui kõik määratud tingimused on väärad, tagastab funktsioon `OR` *kahendmuutuja* väärtuse **FALSE**. Kui mõni määratud tingimustest on tõene, tagastab funktsioon *kahendmuutuja* väärtuse **TRUE**.

## <a name="syntax"></a>Süntaks

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumendid

`condition 1`: *kahendmuutuja*

Kehtiv tingimuslik avaldis, mida tuleb testida. See argument on kohustuslik.

`condition N`: *kahendmuutuja*

Kehtiv tingimuslik avaldis, mida tuleb testida. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*Kahendmuutuja*

Tulemiks saadud *kahendmuutuja* väärtus.

## <a name="example"></a>Näide

`OR (1=2, "a"="a")` tagastab väärtuse **TRUE**.

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
