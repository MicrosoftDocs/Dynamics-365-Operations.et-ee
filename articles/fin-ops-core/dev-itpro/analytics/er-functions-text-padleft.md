---
title: ER-i funktsioon PADLEFT
description: See artikkel annab teavet selle kohta, kuidas kasutatakse PADLEFT-elektroonilise aruandluse (ER) funktsiooni.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 551b508bc6a17b1c6a08e25d5db0094713d9634f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892562"
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