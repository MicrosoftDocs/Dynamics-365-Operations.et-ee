---
title: ER-i funktsioon SPLIT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLIT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e1f11d68b697fdd363f429e60a79f1e1f97bab5b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686388"
---
# <a name="split-er-function"></a>ER-i funktsioon SPLIT

[!include [banner](../includes/banner.md)]

Funktsioon `SPLIT` tükeldab määratud sisendstringid alamstringideks ja tagastab tulemuse uue *kirjete loendi* väärtusena.

## <a name="syntax-1"></a>Süntaks 1

```vb
SPLIT (input, length)
```

Seda süntakstit kasutatakse määratud sisendstringi jaotamiseks alamstringideks, millest igaühel on määratud pikkus.

## <a name="syntax-2"></a>Süntaks 2

```vb
SPLIT (input, delimiter)
```

Seda süntaksit kasutatakse määratud sisendstringi jaotamiseks määratletud eraldaja põhjal alamstringideks.

## <a name="arguments"></a>Argumendid

`input`: *string*

Jaotatav tekst.

`length`: *täisarv*

Ühe alamstringi maksimaalne pikkus.

`delimiter`: *string*

Eraldaja, mida kasutatakse alamstringide eraldamiseks.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Tagastatava loendi kirjete struktuur koosneb tüübi *String* väljast **Väärtus**. Iga tagastatava loendi kirje sisaldab selle välja loodud alamstringe

Kui argument `delimiter` on tühi, koosneb uus loend, mis tagastati, ühest kirjest, millel on tüübi *String* väli **Väärtus**. See väli sisaldab sisestusteksti.

Kui argument `input` on tühi, tagastatakse uus tühi loend. Kui argument `input` või `delimiter` on määratlemata (null), ilmneb rakenduse erand.

## <a name="example-1"></a>Näide 1

`SPLIT ("abcd", 3)` tagastab uue loendi, mis koosneb kahest kirjest, millel on tüübi *String* väli **Väärtus**. Esimese kirje väli **Väärtus** sisaldab teksti **„abc”** ja teise kirje väli **Väärtus** sisaldab teksti **„d”** 

## <a name="example-2"></a>Näide 2

`SPLIT ("XAb aBy", "aB")` tagastab uue loendi, mis koosneb kolmest kirjest, millel on tüübi *String* väli **Väärtus**. Esimese kirje väli **Väärtus** sisaldab teskti **„X”**, välja **Väärtus** teisene kirje sisaldab teksti **„&nbsp;”** ja kolmanda kirje väli **Väärtus** sisaldab teksti **„y”**. 

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)
