---
title: ER-i funktsioon DATETIMEVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATETIMEVALUE.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: cec8f16e683c7eb808fc353830f2baa5c46e31d1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747007"
---
# <a name="datetimevalue-er-function"></a>ER-i funktsioon DATETIMEVALUE

[!include [banner](../includes/banner.md)]

Funktsioon `DATETIMEVALUE` tagastab *kuupäeva ja kellaaja* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva/kellaaja väärtuse [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Süntaks 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Tekst, mis tähistab vormindatavat väärtust.

`format`: *string*

Antud teksti vorming.

`culture`: *string*

Kultuur, mida kasutatakse antud teksti vormindamiseks.

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