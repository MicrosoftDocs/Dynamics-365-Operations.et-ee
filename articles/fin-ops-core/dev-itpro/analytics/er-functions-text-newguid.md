---
title: NEWGUID ER funktsioon
description: See artikkel annab teavet selle kohta, kuidas kasutatakse ER-funktsiooni NEWSEADMETED-elektroonilise aruandluse (ER).
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861812"
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
