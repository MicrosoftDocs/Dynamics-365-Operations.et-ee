---
title: ER-i funktsioon LEFT
description: See artikkel annab teavet selle kohta, kuidas kasutatakse LEFT Electronic Reporting (ER) funktsiooni.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 51842c56053f9de8ea7f65bcda71d606f42f8bf1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852629"
---
# <a name="left-er-function"></a>ER-i funktsioon LEFT

[!include [banner](../includes/banner.md)]

Funktsioon `LEFT` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringi algusest.

## <a name="syntax"></a>Süntaks

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

*Stringi* väärtus, mis tähistab algteksti.

`number`: *täisarv*

Märkide arv, mis tuleb algteksti algusest tagastada.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`LEFT ("Sample", 3)` tagastab tulemuse **„Sam”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]