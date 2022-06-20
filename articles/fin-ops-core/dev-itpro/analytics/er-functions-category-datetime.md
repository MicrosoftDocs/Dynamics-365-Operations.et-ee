---
title: ER-i funktsioonide loend kuupäeva ja kellaaja kategoorias
description: See artikkel annab teavet kuupäeva ja kellaaja funktsioonide kohta, mida elektroonilises aruandluses (ER) toetatakse.
author: NickSelin
ms.date: 09/09/2021
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
ms.openlocfilehash: e6e15d143bad016883f03ecf0125ce9429215a71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880235"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>ER-i funktsioonide loend kuupäeva ja kellaaja kategoorias

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) kuupäeva ja kellaaja funktsioone saab kasutada kuupäeva ja kellaaja väärtustest teabe ekstraktimiseks ning nende kohta toimingute tegemiseks. See artikkel annab nende funktsioonide kokkuvõtte.

## <a name="list-of-supported-functions"></a>Toetatud funktsioonide loend

| Funktsioon | Kirjeldus |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | See funktsioon tagastab *[kuupäeva ja kellaaja](er-formula-supported-data-types-primitive.md#datetime)* väärtuse, mis on määratud alguskuupäevast varasemate või hilisemate päevade arvuna. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | See funktsioon tagastab *DateTime* väärtuse, mis teisendatakse antud ajatsooni kuupäeva/kellaaja väärtusest teise ajatsooni kuupäeva/kellaaja väärtuseks. |
| [DateFormat](er-functions-datetime-dateformat.md) | See funktsioon tagastab *[stringi](er-formula-supported-data-types-primitive.md#string)* väärtuse, mis esitab antud kuupäeva väärtuse määratud vormingus tekstina ja valikuliselt määratletud kultuuris. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | See funktsioon tagastab *stringi* väärtuse, mis esitab antud kuupäeva/kellaaja väärtuse määratud vormingus tekstina ja valikuliselt määratletud kultuuris. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva/kellaaja väärtuse kultuuris. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis teisendatakse määratud kuupäevast väärtusest kuupäeva/kellaaja väärtuseks koordineeritud maailmaajas (Greenwichi aeg \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | See funktsioon tagastab *[kuupäevaväärtuse](er-formula-supported-data-types-primitive.md#date)*, mis teisendatakse antud tekstiväärtusest määratud vormingus ja valikuliselt määratud kultuuri kuupäevaväärtuseks. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | See funktsioon tagastab *[täisarvu](er-formula-supported-data-types-primitive.md#integer)* väärtuse, mis näitab päevade arvu 1. jaanuarist kuni määratud kuupäevani. |
| [Päevi](er-functions-datetime-days.md) | See funktsioon tagastab *täisarvu* väärtuse, mis tähistab ühe määratud kuupäeva ja teise määratud kuupäeva vahelise päevade arvu täisarvuna. |
| [Now](er-functions-datetime-now.md) | Selle funktsiooniga tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakendusserveri praegust kuupäeva ja kellaaega. |
| [NullDate](er-functions-datetime-nulldate.md) | See funktsioon tagastab *kuupäeva* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuaril 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuaril 1900) koordineeritud maailmaajas. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Selle funktsiooniga tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva ja kellaaega. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Selle funktsiooniga tagastab *kuupäeva* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva. |
| [Täna](er-functions-datetime-today.md) | Selle funktsiooniga tagastab *kuupäeva* väärtuse, mis tähistab rakendusserveri praegust kuupäeva. |
| [WeekNum](er-functions-datetime-weeknum.md) | See funktsioon tagastab *täisarvu* väärtuse, mis esindab aasta nädalat. |

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse valemi keel](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
