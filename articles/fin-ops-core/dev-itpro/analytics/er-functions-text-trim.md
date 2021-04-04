---
title: ER-i funktsioon TRIM
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TRIM.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: b671ef72a3558c17fb16db939770394b225656da
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560032"
---
# <a name="trim-er-function"></a>ER-i funktsioon TRIM

[!include [banner](../includes/banner.md)]

Funktsioon `TRIM` tagastab määratud tekstistringi *stringi* väärtusena pärast algus- ja lõputühikute kärpimist ning sõnade vahel olevate mitmekordsete tühikute eemaldamist.

## <a name="syntax"></a>Süntaks

```vb
TRIM (text )
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Tüübi *String* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` tagastab tulemuse **„Näidistekst”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]