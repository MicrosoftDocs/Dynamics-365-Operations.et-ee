---
title: ER-i funktsioon DAYOFYEAR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DAYOFYEAR.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: ab252b6194267836ba9e1d85f3b96fb100c9f598c783bd9c849c6490c2e54e21
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712305"
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