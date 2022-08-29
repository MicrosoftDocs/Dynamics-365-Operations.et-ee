---
title: ER-i funktsioon CH_BANK_MOD_10
description: See artikkel annab teavet selle kohta CH_BANK_MOD_10 kuidas elektroonilise aruandluse (ER) funktsiooni kasutatakse.
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
ms.openlocfilehash: f658228e0c181bab9e07237adc330dbcb13c95c6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288096"
---
# <a name="ch_bank_mod_10-er-function"></a>ER-i funktsioon CH_BANK_MOD_10

[!include [banner](../includes/banner.md)]

Funktsioon `CH_BANK_MOD_10` tagastab *stringi* väärtuse, mis tähistab kreeditori viidet MOD10 avaldisena, mis põhineb määratud arve numbri numbritel.

## <a name="syntax"></a>Süntaks

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumendid

`invoice number digits`: *string*

Teksti väärtus, mis tähistab arve numbri numbreid.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`CH_BANK_MOD_10 ("VEND-200002")` tagastab **3**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
