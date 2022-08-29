---
title: ER-i funktsioon RIGHT
description: See artikkel annab teavet õige elektroonilise aruandluse (ER) funktsiooni kohta.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: fc3e5fed67ecc67bf0673f7d8322b7c151c4d50c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287150"
---
# <a name="right-er-function"></a>ER-i funktsioon RIGHT

[!include [banner](../includes/banner.md)]

Funktsioon `RIGHT` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringi lõpust.

## <a name="syntax"></a>Süntaks

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

*Stringi* väärtus, mis tähistab algteksti.

`number`: *täisarv*

Märkide arv, mis tuleb algteksti lõpust tagastada.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`RIGHT ("Sample", 3)` tagastab **„ple”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
