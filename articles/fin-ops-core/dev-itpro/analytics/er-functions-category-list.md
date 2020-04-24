---
title: ER-i funktsioonide loend loendi kategoorias
description: See teema annab teavet loendi funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
author: NickSelin
manager: kfend
ms.date: 04/01/2020
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
ms.openlocfilehash: dcf1b755959c7ae25928e3f44e988f800027786a
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201039"
---
# <a name="list-of-er-functions-in-the-list-category"></a>ER-i funktsioonide loend loendi kategoorias

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) loendi funktsioone saab kasutada andmete ekstraktimiseks ja toimingute tegemiseks andmetüüpide *Kirjete loend* ja *Konteiner (kirje)* andmeallikates. See teema sisaldab järgmiste funktsioonide kokkuvõtet.

## <a name="list-of-supported-functions"></a>Toetatud funktsioonide loend

| Funktsioon | Kirjeldus |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | See funktsioon töötab mälusisese valikuna. See tagastab uue tasandatud *kirjete loendi* väärtuse, mis koosneb kirjete loendist, mis tähistab kõiki määratud teele vastavaid üksuseid. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | See funktsioon töötab liidetud SQL-päringuna. See tagastab uue tasandatud *kirjete loendi* väärtuse, mis koosneb kirjete loendist, mis tähistab kõiki määratud teele vastavaid üksuseid. |
| [Loendus](er-functions-list-count.md)                       | See funktsioon tagastab *täisarvu* väärtuse, mis tähistab kirjete arvu määratud loendis, kui loend pole tühi. Kui loend on tühi, tagastab funktsioon väärtuse **0** (null). |
| [EmptyList](er-functions-list-emptylist.md)               | See funktsioon tagastab tühja *kirjete loendi* väärtuse, kasutades loendi struktuuri allikana määratud loendit.|
| [Nummerda](er-functions-list-enumerate.md)               | See funktsioon tagastab uue *kirjete loendi* väärtuse, mis koosneb määratud loendi nummerdatud kirjetest. |
| [Filter](er-functions-list-filter.md)                     | See funktsioon tagastab määratud loendi *kirjete loendi* väärtusena pärast seda, kui päringut on muudetud nii, et see filtreerib määratud tingimuse jaoks. |
| [Esimene](er-functions-list-first.md)                       | See funktsioon tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see loend pole tühi. Kui loend on tühi, esitab see funktsioon erandi. |
| [FirstOrNull](er-functions-list-firstornull.md)           | See funktsioon tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see kirje pole tühi. Kui kirje on tühi, tagastab see funktsioon *konteineri (kirje)* väärtuse null. |
| [Index](er-functions-list-index.md)                       | See funktsioon tagastab *konteineri (kirje)* väärtuse, mis on valitud määratud numbrilise indeksi abil määratud loendis. Kui indeks on määratud loendis olevate kirjete vahemikust väljas, annab see funktsioon erandi. |
| [IsEmpty](er-functions-list-isempty.md)                   | Kui määratud loend ei sisalda ühtegi kirjet, tagastab see funktsioon *kahendmuutuja* väärtuse **TRUE**. Muidu tagastab see *kahendväärtuse* **VÄÄR**. |
| [Loend](er-functions-list-list.md)                         | See funktsioon tagastab *kirjete loendi* väärtuse, mis koosneb määratud argumentidest loodud uuest loendist.|
| [ListJoin](er-functions-list-listjoin.md)                 | See funktsioon tagastab *kirjete loendi* väärtuse, mis tähistab määratud argumentidest loodud uut ühendatud loendit.|
| [ListOfFields](er-functions-list-listoffields.md)         | See funktsioon tagastab *kirjete loendi* väärtuse, mis luuakse tüübi *Loetelu* või *Konteiner (kirje)* määratud argumendi struktuuri põhjal. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | See funktsioon tagastab *kirjete loendi* väärtuse, mis koosneb ainult määratud loendi esimesest kirjest.|
| [OrderBy](er-functions-list-orderby.md)                   | See funktsioon tagastab määratud loendi *kirjete loendi* väärtusena, kui see on vastavalt määratud argumentidele sorditud. Neid argumente saab määratleda avaldistena. |
| [Storneeri](er-functions-list-reverse.md)                   | See funktsioon tagastab määratud loendi *kirjete loendi* väärtusena pööratud sortimisjärjestuses. |
| [Tükeldamine](er-functions-list-split.md)                       | See funktsioon tükeldab määratud sisendstringid alamstringideks ja tagastab tulemuse uue *kirjete loendi* väärtusena. |
| [SplitList](er-functions-list-splitlist.md)               | See funktsioon jaotab määratud loendi alamloenditeks (või partiideks), millest igaüks sisaldab määratud kirjete arvu. See tagastab seejärel tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | See funktsioon jaotab määratud loendi alamloendite (partiide) uueks loendiks. Iga partii kirjete arv arvutatakse dünaamiliselt. Funktsioon tagastab tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest. |
| [StringJoin](er-functions-list-stringjoin.md)             | See funktsioon tagastab *stringi* väärtuse, mis koosneb määratud loendi määratud välja liitväärtustest. Väärtused saab eraldada määratud eraldajaga. |
| [Kus](er-functions-list-where.md)                       | See funktsioon tagastab määratud loendi *kirjete loendi* väärtusena, kui see on vastavalt määratud tingimusele filtreeritud. |

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse valemi keel](er-formula-language.md)
