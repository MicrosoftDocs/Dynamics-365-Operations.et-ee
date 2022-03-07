---
title: ER-i funktsioon DATEVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATEVALUE.
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 446f1357e54342073e73f86ef36e6467e029ebc4
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485570"
---
# <a name="datevalue-er-function"></a>ER-i funktsioon DATEVALUE

[!include [banner](../includes/banner.md)]

`DATEVALUE` Funktsioon tagastab *[Kuupäeva](er-formula-supported-data-types-primitive.md#date)* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva väärtuse [kultuuris](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Süntaks 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumendid

`text`: *[String](er-formula-supported-data-types-primitive.md#string)*

Tekst, mis tähistab vormindatavat väärtust.

`format`: *string*

Antud teksti vorming. Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *string*

Kultuur, mida kasutatakse antud teksti vormindamiseks. Lisateabe saamiseks toetatud kultuuride kohta vaata [kultuur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Tagastusväärtused

*Kuupäev*

Tulemiks saadud kuupäeva väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst. Näiteks kui funktsioon `DATEVALUE` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades. Olemi `culture` vaikeväärtus on **EN-US**.

## <a name="example-1"></a>Näide 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` tagastab kuupäeva väärtuse **21. detsember 2016**, mis põhineb määratletud kohandatud vormingul ja vaikerakenduse **EN-US** kultuuril.

## <a name="example-2"></a>Näide 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` tagastab kuupäeva väärtuse **21. jaanuar 2016**, mis põhineb määratletud kohandatud vormingul ja kultuuril.

Stringiga `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` ilmneb aga erand, mis teavitab kasutajat sellest, et seda stringi ei tuvastata määratletud kultuuri kehtiva kuupäeva väärtusena.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
