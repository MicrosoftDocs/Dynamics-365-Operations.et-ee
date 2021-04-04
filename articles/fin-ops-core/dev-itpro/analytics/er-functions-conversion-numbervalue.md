---
title: ER-i funktsioon NUMBERVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMBERVALUE.
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561418"
---
# <a name="numbervalue-er-function"></a>ER-i funktsioon NUMBERVALUE

[!include [banner](../includes/banner.md)]

Funktsioon `NUMBERVALUE` tagastab *tegeliku* väärtuse, mis konverteeritakse määratud *stringi* väärtusest. Teisendamise käigus arvestatakse määratud kümnendkoha ja arvu rühmitamise eraldajaga.

## <a name="syntax"></a>Süntaks

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Teksti väärtus, mis tuleb teisendada *täisarvuliseks* numbriks.

`decimal separator`: string

Komakohaeraldaja. Seda kasutatakse kümnendarvu täisarvu ja murdosa eraldamiseks.

`digit grouping separator`: *string*

Arvu rühmitamise eraldaja. Seda kasutatakse tuhandikeraldajana.

## <a name="return-values"></a>Tagastusväärtused

*Tegelik*

Tulemiks saadud numbriline väärtus.

## <a name="example"></a>Näide

`NUMBERVALUE( "1 234,56", ",", " ")` tagastab **1234,56**.

## <a name="additional-resources"></a>Lisaressursid

[Tüübiteisenduse funktsioonid](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]