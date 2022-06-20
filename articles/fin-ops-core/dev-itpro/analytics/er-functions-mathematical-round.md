---
title: ER-i funktsioon ROUND
description: See artikkel annab teavet selle kohta, kuidas ümardamise elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: NickSelin
ms.date: 10/21/2020
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
ms.openlocfilehash: 5dce96077ab25f8e545bb99d4bed8fc5bba61e2a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905195"
---
# <a name="round-er-function"></a>ER-i funktsioon ROUND

[!include [banner](../includes/banner.md)]

Funktsioon `ROUND` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist määratud arvu komakohtadeni.

## <a name="syntax"></a>Süntaks

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Argumendid

`number`: *tegelik*

Numbriline väärtus, mis tuleb ümardada.

`decimals`: *täisarv*

Arvuline väärtus, mis tähistab kümnendkohtade arvu.

## <a name="return-values"></a>Tagastusväärtused

*Tegelik*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui argumendi `decimals` väärtus on suurem kui 0 (null), ümardatakse määratud number nii paljude komakohtadeni.

Kui argumendi `decimals` väärtus on **0** (null), ümardatakse määratud number lähima paarisarvuni.

Kui argumendi `decimals` väärtus on väiksem kui 0 (null), ümardatakse määratud number komakohast vasakule.

## <a name="example-1"></a>Näide 1

`ROUND (1200.767, 2)` ümardab kahe komakohani ja tagastab väärtuse **1200,77**.

## <a name="example-2"></a>Näide 2

`ROUND (1200.767, -3)` ümardab lähima 1000 kordseni ja tagastab väärtuse **1000**.

## <a name="example-3"></a>Näide 3

`ROUND (1200.5, 0)` ümardab lähima täisarvuni ja tagastab väärtuse **1200**, samas kui `ROUND (1201.5, 0)` teeb sama ja tagastab väärtuse **1202**.

## <a name="additional-resources"></a>Lisaressursid

[Matemaatilised funktsioonid](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]