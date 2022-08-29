---
title: NEWGUID ER funktsioon
description: See artikkel annab teavet selle kohta, kuidas kasutatakse ER-funktsiooni NEWSEADMETED-elektroonilise aruandluse (ER).
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274768"
---
# <a name="newguid-er-function"></a>NEWGUID ER funktsioon

[!include [banner](../includes/banner.md)]

Funktsioon `NEWGUID` loob uue globaalselt kordumatu ID (GUID) ja tagastab selle *[GUID](er-formula-supported-data-types-primitive.md#guid)* väärtusena.

## <a name="syntax"></a>Süntaks

```vb
NEWGUID ()
```

## <a name="return-values"></a>Tagastusväärtused

*GUID*

Tulemiks saadav GUID väärtus.

## <a name="example"></a>Näide

`NEWGUID()` annab alati tulemuseks uue *GUID* väärtuse nagu näiteks **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
