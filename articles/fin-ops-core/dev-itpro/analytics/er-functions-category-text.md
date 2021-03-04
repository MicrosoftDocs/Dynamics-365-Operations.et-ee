---
title: Teksti kategooria ER-i funktsioonide loend
description: See teema annab teavet teksti funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 228620afc81e154eced572f3b6024d6836d00d66
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686023"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Teksti kategooria ER-i funktsioonide loend

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) teksti funktsioone saab kasutada toimingute tegemiseks andmetüübi *String* andmeallikates. See teema sisaldab järgmiste funktsioonide kokkuvõtet.

## <a name="list-of-supported-functions"></a>Toetatud funktsioonide loend

| Funktsioon | Kirjeldus |
|----------|-------------|
| [Char](er-functions-text-char.md) | See funktsioon tagastab *stringi* väärtuse, mis kujutab üksikut märki, millele viitab määratud Unicode’i number. |
| [Ühenda](er-functions-text-concatenate.md) | See funktsioon tagastab kõik määratud tekstistringi *stringi* väärtusena pärast nende üheks stringiks ühendamist. |
| [Vorming](er-functions-text-format.md) | See funktsioon tagastab määratud stringi *stringi* väärtusena pärast seda, kui see vormindati, asendades **%N** esinemiskorrad *N*. argumendiga. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | See funktsioon otsib määratud loetelu andmeallikast konkreetset *loetelu* väärtust, kasutades loendi nime, mis on määratud *stringi* väärtuseks. Kui *loetelu* väärtus leitakse, tagastab funktsioon selle. |
| [GuidValue](er-functions-text-guidvalue.md) | See funktsioon teisendab *stringi* tüübi määratud sisendi andmeüksuseks tüübiga *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | See funktsioon sõelub andmeid vormingus JavaScript Object Notation (JSON), millele pääseb juurde määratud tee kaudu ja see ekstraktib määratud ID-l põhineva skalaarväärtuse. Seejärel tagastab see ekstraktitud skalaarväärtus *stringi* väärtusena. |
| [Vasak](er-functions-text-left.md) | See funktsioon tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringi algusest. |
| [Len](er-functions-text-len.md) | See funktsioon tagastab *täisarvu* väärtuse, mis esindab tähemärkide arvu määratud stringis. |
| [Lower](er-functions-text-lower.md) | See funktsioon tagastab *stringi* väärtusena määratud tekstistringi pärast selle teisendamist väiketäheliseks. |
| [Mid](er-functions-text-mid.md) | See funktsioon tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringis, alustades määratud kohast. |
| [NumberFormat](er-functions-text-numberformat.md) | See funktsioon tagastab *stringi* väärtuse, mis esitab määratud numbri määratud vormingus ja valikuliselt määratletud kultuuris. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | See funktsioon tagastab määratud numbri *stringi* väärtusena pärast selle määratud keeles tekstistringideks kirjutamist (st teisendamist). |
| [PadLeft](er-functions-text-padleft.md) | See funktsioon tagastab määratud pikkusega *stringi* väärtuse, milles määratud stringi algusele on lisatud ühest või mitmest määratud märkide üksusest koosnevad täidismärgid. |
| [QrCode](er-functions-text-qrcode.md) | See funktsioon tagastab *konteineri* väärtuse, mis esitab määratud stringi puhul binaarvormingus ruutkoodi (QR-koodi) pildi. |
| [Asenda](er-functions-text-replace.md) | See funktsioon tagastab määratud tekstistringi *stringi* väärtusena pärast seda, kui kõik või osa sellest on asendatud teise stringiga. |
| [Parem](er-functions-text-right.md) | See funktsioon tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringi lõpust. |
| [Tekst](er-functions-text-text.md) | See funktsioon tagastab määratud arvu *stringi* väärtusena pärast seda, kui see on teisendatud tekstistringiks, mis on vormindatud praeguse rakenduse eksemplari serverilokaadi sätete kohaselt. |
| [Tõlkimine](er-functions-text-translate.md) | See funktsioon tagastab väärtuse *String*, mis sisaldab määratud teksti tähemärkide muu sisestatud märgikomplektiga asendamise tulemust. |
| [Trim](er-functions-text-trim.md) | See funktsioon tagastab määratud tekstistringi *stringi* väärtusena pärast algus- ja lõputühikute kärpimist ning sõnade vahel olevate mitmekordsete tühikute eemaldamist. |
| [Upper](er-functions-text-upper.md) | See funktsioon tagastab *stringi* väärtusena määratud tekstistringi pärast selle teisendamist suurtäheliseks. |

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse valemi keel](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]