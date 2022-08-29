---
title: ER-i funktsioon CN_GBT_ADDITIONALDIMENSIONID
description: See artikkel annab teavet selle kohta CN_GBT_ADDITIONALDIMENSIONID kuidas elektroonilise aruandluse (ER) funktsiooni kasutatakse.
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
ms.openlocfilehash: 0ed2593f865a4764b1c6172722d701a0a10ba5f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281748"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>ER-i funktsioon CN_GBT_ADDITIONALDIMENSIONID

[!include [banner](../includes/banner.md)]

Funktsioon `CN_GBT_ADDITIONALDIMENSIONID` tagastab *stringi* väärtuse, mis tähistab ühte finantsdimensiooni ID-d, mis on määratud stringist võetud. Määratud string esitab kõik dimensioonid komadega eraldatud ID-de loendina.

## <a name="syntax"></a>Süntaks

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

*String* väärtusm mis esitab kõik dimensioonid komadega eraldatud ID-de loendina.

`number`: täisarv

*Täisarvu* väärtus, mis määratleb taotletud dimensiooni seeriakoodi määratud stringis.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` tagastab **„CC”**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
