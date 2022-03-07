---
title: ER-i funktsioon PADLEFT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni PADLEFT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 806b1d318f18b0ade01f7b03909c90b1e4fd29b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746239"
---
# <a name="padleft-er-function"></a>ER-i funktsioon PADLEFT

[!include [banner](../includes/banner.md)]

Funktsioon `PADLEFT` tagastab määratud pikkusega *stringi* väärtuse, milles määratud stringi algusele on lisatud määratud märkidest koosnevad täidismärgid.

## <a name="syntax"></a>Süntaks

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

*Stringi* väärtus, mis tähistab algteksti.

`length`: *täisarv*

*Täisarvu* väärtus, mis tähistab täidismärkidega stringi lõplikku tähemärkide arvu.

`padding chars`: *string*

Täidiseks kasutatavad tähemärgid.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`PADLEFT ("1234", 10, "`&nbsp;`")` tagastab tekstistringi **„&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]