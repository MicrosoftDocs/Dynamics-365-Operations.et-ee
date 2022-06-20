---
title: ER-i funktsioon TRANSLATE
description: See artikkel annab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) TÕLKImise funktsiooni.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: cf44ad5518e2850d4d4e7fd34866ee2f8313c356
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894320"
---
# <a name="translate-er-function"></a>ER-i funktsioon TRANSLATE

[!include [banner](../includes/banner.md)]

Funktsioon `TRANSLATE` tagastab väärtuse *String*, mis sisaldab määratud teksti tähemärkide muu sisestatud märgikomplektiga asendamise tulemust.

## <a name="syntax"></a>Süntaks

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Tüübi *String* andmeallika kehtiv tee.

`pattern`: *string*

Tekst, mis tuleb asendada.

`replacement`: *string*

Asendamiseks kasutatav tekst.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Funktsioon `TRANSLATE` asendab ühe tähemärgi korraga. Funktsioon asendab argumendi `text` esimese tähemärgi argumendi `pattern` esimese tähemärgiga ja seejärel asendab kõik ülejäänud tähemärgid sama moodi. Kui argumentide `text` ja `pattern` tähemärgid ühtivad, asendatakse argumendi `pattern` tähemärk argumendi `replacement` samas kohas asuva tähemärgiga. Kui tähemärk kuvatakse argumendis `pattern` mitu korda, kasutatakse selle tähemärgi esimesele esinemisele vastavat argumendi `replacement` vastendust.

## <a name="example-1"></a>Näide 1

`TRANSLATE ("abcdef", "cd", "GH")` asendab määratud teksti **„abcdef”** tähemärgi **„c”** teksti `replacement` tähemärgiga **„G”** järgmistel põhjustel.
-   Tähemärk **„c”** asub tekstis `pattern` esimesel positsioonil.
-   Teksti `replacement` esimesel positsioonil asub tähemärk **„G”**.

## <a name="example-2"></a>Näide 2

`TRANSLATE ("abcdef", "ccd", "GH")` tagastab **„abGdef”**.

## <a name="example-3"></a>Näide 3

`TRANSLATE ("abccba", "abc", "123")` tagastab **„123321”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]