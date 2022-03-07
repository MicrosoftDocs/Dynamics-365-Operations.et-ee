---
title: ER-i funktsioon CASE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CASE
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 97f5e821a635d5d31092a7b27f7ae3c2e603462186449bab5856955371a7f613
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756401"
---
# <a name="case-er-function"></a>ER-i funktsioon CASE

[!include [banner](../includes/banner.md)]

Funktsioon `CASE` arvutab määratud avaldise väärtuse määratud teise suvandi suhtes ja tagastab esimese suvandi tulemuse, mis on võrdne määratud avaldise väärtusega. Vastasel juhul tagastab see valikulise vaikimisi tulemuse, kui vaikimisi tulemus on määratud kutsutud funktsiooni viimaseks argumendiks, millele ei eelne suvandit. Tagastatav väärtus võib olla toetatud andmetüüpide mis tahes väärtus.

## <a name="syntax"></a>Süntaks

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumendid

`expression`: *primitiivne andmetüüp* (kahendmuutuja, numbriline või tekst)

Kehtiv avaldis, mis tagastab primitiivse andmetüübi väärtuse.

`option 1`: *primitiivne andmetüüp* (kahendmuutuja, numbriline või tekst)

Kehtiv avaldis, mis tagastab sama primitiivse andmetüübi väärtuse kui kutsutud funktsiooni argument `expression`. See argument on kohustuslik.

`result 1`: *mis tahes toetatud andmetüüp*

Tagastatav tulemus, mis vastab eelmisele valikule. See argument on kohustuslik.

`option N`: *primitiivne andmetüüp* (kahendmuutuja, numbriline või tekst)

Kehtiv avaldis, mis tagastab sama primitiivse andmetüübi väärtuse kui kutsutud funktsiooni argument `expression`. See argunent on valikuline.

`result N`: *mis tahes toetatud andmetüüp*

Tagastatav tulemus, mis vastab eelmisele valikule. See argunent on valikuline.

`default result`: *mis tahes toetatud andmetüüp*

Tulemus, mis tuleks tagastada, kui vastet pole. See argunent on valikuline.

## <a name="return-values"></a>Tagastusväärtused

*Mis tahes toetatud andmetüüp*

Mis tahes toetatud andmetüübi tulemuseks olev väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Käitusajal esitatakse erand, kui puudub vaste ja valikuline vaikimisi tulemus pole määratletud.

Kõik tulemused tuleb määrata sama andmetüüpi kasutades. Kujundamise ajal esitatakse erand, kui konfigureeritud tulemuste andmetüübid ei ühti.

Kui esimese tulemuse väärtus ja *N*. tulemuse väärtus on andmetüübi *Konteiner (kirje)* või *Kirjete loend* väärtused, on tulemuses ainult väljad, mis eksisteerivad mõlemas väärtuses.

## <a name="example"></a>Näide

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` tagastab stringi **„WINTER”**, kui praeguse rakenduse seansi kuupäev jääb vahemikku oktoober kuni detsember. Muidu tagastatakse tühi string.

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]