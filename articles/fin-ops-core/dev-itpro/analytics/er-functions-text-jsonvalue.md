---
title: ER-i funktsioon JSONVALUE
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni JSONVALUE Electronic Reporting (ER).
author: kfend
ms.date: 10/25/2021
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
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267959"
---
# <a name="jsonvalue-er-function"></a>ER-i funktsioon JSONVALUE

[!include [banner](../includes/banner.md)]

Funktsioon `JSONVALUE` sõelub andmeid vormingus JavaScript Object Notation (JSON), millele pääseb juurde määratud tee kaudu ja see ekstraktib skalaarväärtuse, millel on määratud ID. Seejärel tagastab see ekstraktitud skalaarväärtus *stringi* väärtusena.

## <a name="syntax"></a>Süntaks

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumendid

`input`: *string*

Tüübi *String* andmeallika kehtiv tee, mis sisaldab JSON-andmeid.

`path`: *string*

JSON-andmete skalaarväärtuse identifikaator. Seotud JSON-sõlmede nimede lahutamiseks kasutage kaldkriipsu (/). Kasutage sulgude (\[\]) märget JSON-massiivi väärtuse indeksi määramiseks. Pange tähele, et selles indeksis kasutatakse null-põhist nummerdamist.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example-1"></a>Näide 1

Andmeallikas **JsonField** sisaldab JSON-vormingus järgmisi andmeid: **{„BuildNumber”:„7.3.1234.1”, „KeyThumbprint”:„7366E”}**. Sellisel juhul tagastab avaldis `JSONVALUE (JsonField, "BuildNumber")` järgmise andmetüübi *String* väärtuse: **„7.3.1234.1”**.

## <a name="example-2"></a>Näide 2

*Arvutatud väli* andmeallikas **JsonField** sisaldab järgmist avaldist: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

See avaldis on konfigureeritud tagastama [*Stringi*](er-formula-supported-data-types-primitive.md#string) väärtust, mis esindab JSON-vormingus järgmisi andmeid.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

Sellisel juhul tagastab avaldis `JSONVALUE(json, "workers/[1]/emails/[0]")` järgmise andmetüübi *String* väärtuse: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
