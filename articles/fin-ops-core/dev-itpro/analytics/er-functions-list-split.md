---
title: ER-i funktsioon SPLIT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLIT.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 4a42b0c7cfa2a8d3dcb7448224c9e88a48276f7d8cdbcce484383a778b8275a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757317"
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

## <a name="example-3"></a>Näide 3

Funktsiooni [INDEX](er-functions-list-index.md) abil pääsete juurde määratud sisendstringi üksikutele elementidele. Kui sisestate tüübi **Arvutatud väli** andmeallika **MyList** ja konfigureerida seda `SPLIT("abc", 1)` avaldisele, tagastab see `INDEX(MyList,2).Value` teksti väärtuse **„b”**.

## <a name="example-4"></a>Näide 4

Funktsiooni [ENUMERATE](er-functions-list-enumerate.md) abil pääsete juurde määratud sisendstringi üksikutele elementidele. Kui sisestate esmalt tüübi **Arvutatud väli** andmeallika **MyList** ja konfigureerite selle `SPLIT("abc", 1)` avaldise ning seejärel sisestate tüübi **Arvutatud väli** andmetüübi **EnumeratedList** andmeallika ja konfigureerite selle `ENUMERATE(MyList)` avaldise, tagastab avaldis `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` teksti **„b”**.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
