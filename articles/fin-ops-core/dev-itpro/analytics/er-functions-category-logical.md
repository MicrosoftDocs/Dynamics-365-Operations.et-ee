---
title: ER-i funktsioonide loend loogilises kategoorias
description: See teema annab teavet loogiliste funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
author: NickSelin
ms.date: 02/11/2021
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
ms.openlocfilehash: 43cbecf80ff70dac058977932c3a0bb03662cd98a88c68407051bdc584609d84
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767190"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>ER-i funktsioonide loend loogilises kategoorias

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) loogilisi funktsioone saab kasutada loogiliste väärtustega töötamiseks, et teostada rohkem kui ühe võrdluse ühe avaldisega või mitme tingimuse testimiseks. See teema sisaldab järgmiste funktsioonide kokkuvõtet.

## <a name="list-of-supported-functions"></a>Toetatud funktsioonide loend

| Funktsioon | Kirjeldus |
|----------|-------------|
| [Ja](er-functions-logical-and.md)                       | Kui kõik määratud tingimused on tõesed, tagastab see funktsioon *kahendmuutuja* väärtuse **TRUE**. Muidu tagastab see *kahendväärtuse* **VÄÄR**. |
| [Kast](er-functions-logical-case.md)                     | See funktsioon arvutab määratud avaldise väärtuse määratud teise suvandi suhtes ja tagastab esimese suvandi tulemuse, mis on võrdne määratud avaldise väärtusega. Vastasel juhul tagastab see valikulise vaikimisi tulemuse, kui vaikimisi tulemus on määratud kutsutud funktsiooni viimaseks argumendiks, millele ei eelne suvandit. Tagastatav väärtus võib olla toetatud andmetüüpide mis tahes väärtus. |
| [Sisaldab](er-functions-logical-contains.md)             | See funktsioon määratleb, kas määratud sisestus algab määratud tekstiga. See toob *Tõeväärtus* väärtuseks **Tõde** määratud sisestusteksti, kui see algab määratud tekstiga. Muidu tagastab see *kahendväärtuse* **VÄÄR**. |
| [Lõpeb](er-functions-logical-endswith.md)             | See funktsioon määratleb, kas määratud sisestus algab määratud tekstiga. See toob *Tõeväärtus* väärtuseks **Tõde** määratud sisestusteksti, kui see algab määratud tekstiga. Muidu tagastab see *kahendväärtuse* **VÄÄR**. |
| [Kui](er-functions-logical-if.md)                         | See funktsioon annab vastuseks esimese määratud väärtuse, kui määratud tingimus on täidetud. Muul juhul annab see vastuseks teise määratud väärtuse. Tagastatav väärtus võib olla toetatud andmetüüpide mis tahes väärtus. |
| [Ei ole](er-functions-logical-not.md)                       | See funktsioon annab määratud tingimuse pööratud loogilise väärtuse *kahendmuutuja* väärtusena. |
| [Or](er-functions-logical-or.md)                         | Kui kõik määratud tingimused on väärad, tagastab see funktsioon *kahendmuutuja* väärtuse **FALSE**. Kui mõni määratud tingimustest on tõene, tagastab funktsioon *kahendmuutuja* väärtuse **TRUE**. |
| [Alustab](er-functions-logical-startswith.md)         | See funktsioon määratleb, kas määratud sisestus algab määratud tekstiga. See toob *Tõeväärtus* väärtuseks **Tõde** määratud sisestusteksti, kui see algab määratud tekstiga. Muidu tagastab see *kahendväärtuse* **VÄÄR**. |
| [ValueIn](er-functions-logical-valuein.md)               | See funktsioon määratleb, kas määratud sisend vastab määratud loendis määratud üksuse mis tahes väärtusele. See tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul. Muidu tagastab see *kahendväärtuse* **VÄÄR**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | See funktsioon määratleb, kas määratud *Int64* või *Täisarv*-tüüpi sisend vastab määratud loendis määratud üksuse mis tahes väärtusele. See tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul. Muidu tagastab see *kahendväärtuse* **VÄÄR**. |


## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse valemi keel](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]