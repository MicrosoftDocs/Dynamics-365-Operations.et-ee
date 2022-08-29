---
title: Funktsioon WEEKNUM ER
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni WEEKNUM Electronic Reporting (ER).
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268142"
---
# <a name="weeknum-er-function"></a>Funktsioon WEEKNUM ER

[!include [banner](../includes/banner.md)]

Funktsioon `WEEKNUM` tagastab täisarvu *[väärtuse](er-formula-supported-data-types-primitive.md#integer)*, mis tähistab aasta nädalat, mis sisaldab määratud kuupäevaväärtust *[...](er-formula-supported-data-types-primitive.md#date)*. Arvutus põhineb kultuurist sõltuvatel reeglitel, mis määratlevad kalendrinädala ja nädala esimese päeva.

## <a name="syntax"></a>Süntaks

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumendid</a>

`date`: *kuupäev*

Kuupäevaväärtus, mis tähistab kuupäeva, mida kasutatakse aasta nädala arvutamiseks.

`culture`: *[string](er-formula-supported-data-types-primitive.md#string)*

Kalkulatsiooniks salvestatud kultuur. Saate kasutada kultuurikoode, mida toetatakse vastavalt .NET-standarditele [...](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Tagastusväärtused

*Täisarv*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Aasta nädal [arvutatakse vastavalt ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) standardile, kui selle standardi on vastu võtnud riik või regioon, kus lokaadi käitusajal esitatakse. Muul juhul põhineb arvutus riigi-/regioonipõhistel riiklikel standarditel.

Kui käitusajal [esitatakse](#arguments) funktsiooni argumendina `WEEKNUM` toetuseta kultuurikood, ilmneb erand. Kui kultuurikoodina esitatakse tühi string, kasutatakse nädalanumbri arvutamiseks Inglise riigi-neutraalset kalendrit.

## <a name="examples"></a>Näited

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` tagastab **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` tagastab **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` tagastab **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` tagastab **21**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
