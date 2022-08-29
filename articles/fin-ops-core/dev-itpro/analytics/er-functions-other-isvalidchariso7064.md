---
title: ER-i funktsioon ISVALIDCHARACTERISO7064
description: See artikkel annab teavet ISVALIDCHARACTERTOOL7064 elektroonilise aruandluse (ER) funktsiooni kasutamise kohta.
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
ms.openlocfilehash: 26ee54d1c3cd5673ec573e2df688780d3902b69d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275371"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ER-i funktsioon ISVALIDCHARACTERISO7064

[!include [banner](../includes/banner.md)]

Funktsioon `ISVALIDCHARACTERISO7064` tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud string tähistab kehtivat rahvusvahelist pangakonto numbrit (IBAN). Muidu tagastab see *kahendväärtuse* **VÄÄR**.

## <a name="syntax"></a>Süntaks

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

IBAN-i tähistav teksti väärtus.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` tagastab väärtuse **TRUE**. 

`ISVALIDCHARACTERISO7064 ("AT61")` tagastab väärtuse **FALSE**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
