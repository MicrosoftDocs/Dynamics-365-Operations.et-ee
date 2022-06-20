---
title: ER-i funktsioon MID
description: See artikkel annab teavet SELLE kohta, kuidas kasutatakse MID-elektroonilise aruandluse (ER) funktsiooni.
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
ms.openlocfilehash: ca5dbfb6de3057ad2c4a6dcc7ecce3d0ddc69595
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867636"
---
# <a name="mid-er-function"></a>ER-i funktsioon MID

[!include [banner](../includes/banner.md)]

Funktsioon `MID` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringist, alustades määratud kohast.

## <a name="syntax"></a>Süntaks

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

*Stringi* väärtus, mis määrab teksti, millest märke tagastada.

`starting position`: *täisarv*

*Täisarvu* väärtus, mis määrab esimese märgi ametikoha, mis tuleb määratud tekstist tagastada.

`number of characters`: *täisarv*

*Täisarvu* väärtus, mis määrab märkide arvu, mis tuleb tagastada, alustades määratud lähtepositsioonist.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui argumendi `starting position` väärtus on väiksem kui 0 (null), loendatakse tagastatavaid märke määratud stringi esimesest positsioonist.

Kui argumendi `starting position` väärtus ületab määratud stringi pikkust, tagastatakse tühi string.

## <a name="example"></a>Näide

`MID ("Sample", 2, 3)` tagastab **„amp”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]