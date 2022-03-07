---
title: ER-i funktsioon NUMERALSTOTEXT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMERALSTOTEXT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 76431642a6d6961c5c9a2bf15534ad58f83d312dfb3723e75c94fa844717930b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719413"
---
# <a name="numeralstotext-er-function"></a>ER-i funktsioon NUMERALSTOTEXT

[!include [banner](../includes/banner.md)]

Funktsioon `NUMERALSTOTEXT` tagastab määratud numbri *stringi* väärtusena pärast selle määratud keeles tekstistringideks kirjutamist (st teisendamist).

## <a name="syntax"></a>Süntaks

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumendid

`number`: *täisarv* või *tegelik*

Numbriline väärtus, mis määrab arvu, mis tuleb välja kirjutada.

`language`: *string*

*Stringi* väärtus, mis tähistab keelekoodi.

`currency`: *string*

*Stringi* väärtus, mis tähistab valuutakoodi.

`print currency name flag`: *kahendmuutuja*

*Kahendmuutuja* väärtus, mis näitab, kas valuuta nimi peab olema lisatud väljakirjutatud tekstile.

`decimal points`: *täisarv*

*Täisarvu* väärtus, mis näitab kümnendkohtade arvu, mis väljakirjutatud tekstil peab olema.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Keelekood ei ole kohustuslik. Kui see on määratletud tühja stringina, kasutatakse käitatava konteksti keelekoodi. Vaikimisi keelekood on **EN-US**. Käitatava konteksti keelekood on määratletud töötava elektroonilise aruandluse (ER) vormingu elemendis **Kaust** või **Fail**.

Valuutakood ei ole kohustuslik. Kui see on määratletud tühja stringina, kasutatakse käitatava konteksti ettevõtte valuutat.

> [!NOTE] 
> Argumente `print currency name flag` ja `decimal points` analüüsitakse ainult järgmiste keelekoodide puhul: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** ja **RU**. Peale selle analüüsitakse argumenti `print currency name flag` ainult nende ettevõtete puhul, mille riigi või piirkonna kontekst toetab valuuta nimede käänamist.

## <a name="example-1"></a>Näide 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` tagastab vastuse **„One Thousand Two Hundred Thirty Four and 56”**.

## <a name="example-2"></a>Näide 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` tagastab vastuse **Sto dwadzieścia**. 

## <a name="example-3"></a>Näide 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` tagastab vastuse **„Сто двадцать евро 21 евроцент”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]