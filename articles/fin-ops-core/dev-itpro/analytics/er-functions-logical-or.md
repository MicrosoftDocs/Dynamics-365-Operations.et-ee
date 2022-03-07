---
title: ER-i funktsioon OR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni OR.
author: NickSelin
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
ms.openlocfilehash: 9763cdbabfbaba1af433c1fd753b03982ecb550d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751709"
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