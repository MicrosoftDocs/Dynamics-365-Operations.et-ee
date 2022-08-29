---
title: ER-i funktsioon FA_SUM
description: See artikkel annab teavet selle kohta FA_SUM kuidas elektroonilise aruandluse (ER) funktsiooni kasutatakse.
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
ms.openlocfilehash: bcedbc3df835b219b8df6d05f1db6b331f1e9254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278913"
---
# <a name="fa_sum-er-function"></a>ER-i funktsioon FA_SUM

[!include [banner](../includes/banner.md)]

Funktsioon `FA_SUM` tagastab *konteineri (kirje)* väärtuse, mis koosneb põhivara summade andmetest määratud põhivara kauba, väärtusmudeli koodi ja kuupäevade perioodi kohta.

## <a name="syntax"></a>Süntaks

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumendid

`fixed asset code`: *string*

*Stringi* väärtus, mis tähistab põhivara kauba koodi, mille jaoks saldo arvutatakse.

`value model code`: *string*

*Stringi* väärtus, mis tähistab väärtusmudeli koodi, mille jaoks saldo arvutatakse.

`start date`: *kuupäev*

*Kuupäeva* väärtus, mis tähistab selle perioodi alguskuupäeva, mille kohta põhivara summad arvutatakse.

`end date`: *kuupäev*

*Kuupäeva* väärtus, mis tähistab selle perioodi lõpukuupäeva, mille kohta põhivara summad arvutatakse.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="example"></a>Näide

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` tagastab põhivara **COMP-000001** andmekonteineri,m mis on valmistatud ette väärtuse mudelile **Praegune** ja ajavahemikule alates **Date1** kuni **Date2**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
