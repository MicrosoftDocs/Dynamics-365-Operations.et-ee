---
title: ER-i funktsioonide loend kuupäeva ja kellaaja kategoorias
description: See teema annab teavet kuupäeva ja kellaaja funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 2745298ae1f6787c3de5a4aaf6a2a6350f5f3e85
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686215"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>ER-i funktsioonide loend kuupäeva ja kellaaja kategoorias

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) kuupäeva ja kellaaja funktsioone saab kasutada kuupäeva ja kellaaja väärtustest teabe ekstraktimiseks ning nende kohta toimingute tegemiseks. See teema sisaldab järgmiste funktsioonide kokkuvõtet.

## <a name="list-of-supported-functions"></a>Toetatud funktsioonide loend

| Funktsioon | Kirjeldus |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis on määratud alguskuupäevast varasemate või hilisemate päevade arv. |
| [DateFormat](er-functions-datetime-dateformat.md) | See funktsioon tagastab *stringi* väärtuse, mis esitab antud kuupäeva väärtuse määratud vormingus tekstina ja valikuliselt määratletud kultuuris. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | See funktsioon tagastab *stringi* väärtuse, mis esitab antud kuupäeva/kellaaja väärtuse määratud vormingus tekstina ja valikuliselt määratletud kultuuris. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva/kellaaja väärtuse kultuuris. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis teisendatakse määratud kuupäevast väärtusest kuupäeva/kellaaja väärtuseks koordineeritud maailmaajas (Greenwichi aeg \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | See funktsioon tagastab *kuupäeva* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva väärtuse kultuuris. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | See funktsioon tagastab *täisarvu* väärtuse, mis tähistab 1. jaanuari ja määratud kuupäeva vahelise päevade arvu täisarvuna. |
| [Päevi](er-functions-datetime-days.md) | See funktsioon tagastab *täisarvu* väärtuse, mis tähistab ühe määratud kuupäeva ja teise määratud kuupäeva vahelise päevade arvu täisarvuna. |
| [Now](er-functions-datetime-now.md) | Selle funktsiooniga tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakendusserveri praegust kuupäeva ja kellaaega. |
| [NullDate](er-functions-datetime-nulldate.md) | See funktsioon tagastab *kuupäeva* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuaril 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuaril 1900) koordineeritud maailmaajas. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Selle funktsiooniga tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva ja kellaaega. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Selle funktsiooniga tagastab *kuupäeva* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva. |
| [Täna](er-functions-datetime-today.md) | Selle funktsiooniga tagastab *kuupäeva* väärtuse, mis tähistab rakendusserveri praegust kuupäeva. |

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse valemi keel](er-formula-language.md)
