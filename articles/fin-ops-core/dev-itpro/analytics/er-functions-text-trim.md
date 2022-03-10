---
title: ER-i funktsioon TRIM
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TRIM.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: 816f6d6623bb778c9186d294c9b67db7edddd671
ms.sourcegitcommit: 753714ac0dabc4b7ce91509757cd19f7be4a4793
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367788"
---
# <a name="trim-er-function"></a>ER-i funktsioon TRIM

[!include [banner](../includes/banner.md)]

Funktsioon `TRIM` tagastab *määratud tekstistringi stringiväärtusena* pärast vahekaarti, tagastuse, rea toide ja vormi söötmise märgid on asendatud ühe tühikuga, pärast seda kui ees- ja lõputühikud on kärbitud ja pärast mitme tühiku eemaldamist sõnade vahel.

## <a name="syntax"></a>Süntaks

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Tüübi *String* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Mõnel juhul võite soovida kärpida ees- ja lõputühikuid, kuid eelistate valitud teksti jaoks vormindamist säilitada. Näiteks kui see tekst tähistab aadressi, mida saab sisestada mitmerealisele tekstiväljale ja see võib sisaldada rea söötmise ja veose tagastusvormingut. Sellisel juhul kasutage järgmist avaldist: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` kus `text` on määratud tekstistringile viiv argument.

## <a name="example-1"></a>Näide 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` tagastab tulemuse **„Näidistekst”**.

## <a name="example-2"></a>Näide 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` tagastab **väärtuse "Näidistekst"**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)

[ER-i funktsioon REPLACE](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
