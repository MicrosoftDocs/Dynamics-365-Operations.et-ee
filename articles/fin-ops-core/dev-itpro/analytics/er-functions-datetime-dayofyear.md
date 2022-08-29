---
title: ER-i funktsioon DAYOFYEAR
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni DAYOFYEAR Electronic Reporting (ER).
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: e49a80b2ef3c7defcfc23e868374cec5832dc913
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292552"
---
# <a name="dayofyear-er-function"></a>ER-i funktsioon DAYOFYEAR

[!include [banner](../includes/banner.md)]

Funktsioon `DAYOFYEAR` tagastab *täisarvu* väärtuse, mis tähistab 1. jaanuari ja määratud kuupäeva vahelise päevade arvu täisarvuna.

## <a name="syntax"></a>Süntaks

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumendid

`date`: *kuupäev*

Kuupäeva väärtus, mis tähistab päevade arvu arvutamiseks kasutatavat kuupäeva

## <a name="return-values"></a>Tagastusväärtused

*Täisarv*

Tulemiks saadud numbriline väärtus.

## <a name="example-1"></a>Näide 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` tagastab **61**.

## <a name="example-2"></a>Näide 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` tagastab **1**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
