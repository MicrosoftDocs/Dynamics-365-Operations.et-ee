---
title: ER-i funktsioon INDEX
description: See artikkel annab teavet INDEX-i elektroonilise aruandluse (ER) funktsiooni kohta.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 051a2818d862c3bc517e8c20a1742c2599c3bba6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854781"
---
# <a name="index-er-function"></a>ER-i funktsioon INDEX

[!include [banner](../includes/banner.md)]

Funktsioon `INDEX` tagastab *konteineri (kirje)* väärtuse, mis on valitud määratud numbrilise indeksi abil määratud loendis. Kui indeks on määratud loendis olevate kirjete vahemikust väljas, tehakse erand.

## <a name="syntax"></a>Süntaks

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`index`: *täisarv*

Numbriline indeks, mis näitab soovitud kirje asukohta määratud loendis.

> [!NOTE]
> Kuna selle funktsiooni puhul kasutatakse ühe põhinumbrit, määrake määratud loendi esimese kirje tagastamiseks väärtus **1**.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="example-1"></a>Näide 1

Kui sisestate andmeallika **DS** tüübile *Arvutatud väli* ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `DS.Value` selle kirjete loendi teisele kirjele teksti väärtuse **„B”**. Avaldis `INDEX (SPLIT ("A|B|C", "|"), 2).Value` tagastab samuti tekstiväärtuse **„B”**.

## <a name="example-2"></a>Näide 2

Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `INDEX (SPLIT ("A|B|C", "|"), 4).Value` käitusajal erandi.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
