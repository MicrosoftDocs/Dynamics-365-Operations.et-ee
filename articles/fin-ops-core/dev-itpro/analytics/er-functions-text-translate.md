---
title: ER-i funktsioon TRANSLATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TRANSLATE.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 415444bda097c00522155d1b37988a79da836902
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201108"
---
# <a name=""></a><a name="TRANSLATE">ER-i funktsioon TRANSLATE</a>

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
