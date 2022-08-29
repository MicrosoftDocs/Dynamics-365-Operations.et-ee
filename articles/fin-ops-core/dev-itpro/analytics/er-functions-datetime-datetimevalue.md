---
title: ER-i funktsioon DATETIMEVALUE
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni DATETIMEVALUE Electronic Reporting (ER).
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: 591c707ae7f57236386de0b4ef85d428c9ae31fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287334"
---
# <a name="datetimevalue-er-function"></a>ER-i funktsioon DATETIMEVALUE

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE` Funktsioon tagastab *[kuupäeva ja kellaaja](er-formula-supported-data-types-primitive.md#datetime)* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva/kellaaja väärtuse [kultuuris](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Süntaks 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumendid

`text`: *[String](er-formula-supported-data-types-primitive.md#string)*

Tekst, mis tähistab vormindatavat väärtust.

`format`: *string*

Antud teksti vorming. Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *string*

Kultuur, mida kasutatakse antud teksti vormindamiseks. Lisateabe saamiseks toetatud kultuuride kohta vaata [kultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Tagastusväärtused

*DateTime*

Tulemiks saadud kuupäeva/kellaaja väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst. Näiteks kui funktsioon `DATETIMEVALUE` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades. Olemi `culture` vaikeväärtus on **EN-US**.

## <a name="example-1"></a>Näide 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` tagastab tulemuse **2:55:00 21. detsembril 2016**, mis põhineb määratletud kohandatud vormingul ja vaikerakenduse **EN-US** kultuuril.

## <a name="example-2"></a>Näide 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` tagastab tulemuse **2:55:00 21. detsembril 2016**, mis põhineb määratletud kohandatud vormingul ja kultuuril.

Stringiga `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` ilmneb aga erand, mis teavitab kasutajat sellest, et seda stringi ei tuvastata määratletud kultuuri kehtiva kuupäeva/kellaaja väärtusena.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
