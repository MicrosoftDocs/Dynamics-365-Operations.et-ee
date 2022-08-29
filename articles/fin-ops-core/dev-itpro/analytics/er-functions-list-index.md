---
title: ER-i funktsioon INDEX
description: See artikkel annab teavet INDEX-i elektroonilise aruandluse (ER) funktsiooni kohta.
author: kfend
ms.date: 05/20/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 1ecac869644b09ee6564a4cd0eb53a82de9df25f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274022"
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
