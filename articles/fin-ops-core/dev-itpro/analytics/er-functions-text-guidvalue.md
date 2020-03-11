---
title: ER-i funktsioon GUIDVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni GUIDVALUE.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a7b8c782aff488a433c40a49ab7f4fe2d0e944e4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041159"
---
# <a name="GUIDVALUE">ER-i funktsioon GUIDVALUE</a>

[!include [banner](../includes/banner.md)]

Funktsioon `GUIDVALUE` teisendab *stringi* tüübi määratud sisendi andmeüksuseks tüübiga *GUID*.

## <a name="syntax"></a>Süntaks

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumendid

`input`: *string*

Tüübi *String* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*GUID*

Tulemuseks olev globaalselt kordumatu ID (GUID) väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Selleks, et teisendada vastupidises suunas (see tähendab andmetüübi *GUID* määratletud sisendi teisendamiseks andmetüübi *String* andmeüksuseks), saate kasutada funktsiooni [TEXT](er-functions-text-text.md).

## <a name="example"></a>Näide

Määratlege oma mudelivastenduses järgmised andmeallikad.

- Tüübi *Arvutatud väli* andmeallikas **myID**, mis sisaldab avaldist `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- Tüübi **Tabelikirjed** andmeallikas *Kasutajad*, mis viitab tabelile UserInfo

Seejärel saate kasutada avaldist, näiteks `FILTER (Users, Users.objectId = myID)`, tabeli UserInfo filtreerimiseks andmetüübi *GUID* välja **objectId** alusel.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)
