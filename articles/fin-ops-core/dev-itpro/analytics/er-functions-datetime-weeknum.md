---
title: Funktsioon WEEKNUM ER
description: See teema annab teavet selle kohta, kuidas kasutatakse funktsiooni WEEKNUM Electronic Reporting (ER).
author: NickSelin
ms.date: 12/03/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: fe36d4142b6e4922e2cbca09bb0ca9f68f6680a0
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891365"
---
# <a name="weeknum-er-function"></a>Funktsioon WEEKNUM ER

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funktsioon `WEEKNUM` tagastab *[täisarvu](er-formula-supported-data-types-primitive.md#integer)* väärtuse, mis tähistab aasta nädalat, mis sisaldab määratud *[...](er-formula-supported-data-types-primitive.md#date)* kuupäevaväärtust. Arvutus põhineb kultuurist sõltuvatel reeglitel, mis määratlevad kalendrinädala ja nädala esimese päeva.

## <a name="syntax"></a>Süntaks

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumendid</a>

`date`: *kuupäev*

Kuupäevaväärtus, mis tähistab kuupäeva, mida kasutatakse aasta nädala arvutamiseks.

`culture`: *[string](er-formula-supported-data-types-primitive.md#string)*

Kalkulatsiooniks salvestatud kultuur. Saate kasutada kultuurikoode, mida toetatakse vastavalt [.NET-standarditele.](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0)

## <a name="return-values"></a>Tagastusväärtused

*Täisarv*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Aasta nädal arvutatakse vastavalt ISO 8601 standardile, kui selle standardi on vastu võtnud riik või regioon, [kus lokaadi käitusajal](https://www.iso.org/iso-8601-date-and-time-format.html) esitatakse. Muul juhul põhineb arvutus riigi-/regioonipõhistel riiklikel standarditel.

Kui käitusajal esitatakse funktsiooni `WEEKNUM` argumendina toetuseta [kultuuri](#arguments) kood, ilmneb erand. Kui kultuurikoodina esitatakse tühi string, kasutatakse nädalanumbri arvutamiseks Inglise riigi-neutraalset kalendrit.

## <a name="examples"></a>Näited

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` tagastab **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` tagastab **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` tagastab **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` tagastab **21**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
