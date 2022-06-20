---
title: ER-i funktsioon JSONVALUE
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni JSONVALUE Electronic Reporting (ER).
author: NickSelin
ms.date: 10/25/2021
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
ms.openlocfilehash: 7deaed83959f033d11333efb5a2b398cbe57076d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909496"
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
