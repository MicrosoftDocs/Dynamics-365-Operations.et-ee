---
title: ER-i funktsioon TRIM
description: See artikkel annab teavet TRIM-i elektroonilise aruandluse (ER) funktsiooni kohta.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273094"
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
