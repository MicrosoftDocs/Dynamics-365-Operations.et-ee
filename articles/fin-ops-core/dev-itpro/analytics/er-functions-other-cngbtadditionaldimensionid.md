---
title: ER-i funktsioon CN_GBT_ADDITIONALDIMENSIONID
description: See artikkel annab teavet selle kohta CN_GBT_ADDITIONALDIMENSIONID kuidas elektroonilise aruandluse (ER) funktsiooni kasutatakse.
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
ms.openlocfilehash: 80ce6846cd4687c2a12815ef0da1e1684c57d1f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898765"
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