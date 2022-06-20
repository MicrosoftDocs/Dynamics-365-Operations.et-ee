---
title: ER-i funktsioon ROUNDUP
description: See artikkel annab teavet selle kohta, kuidas ümardamise elektroonilise aruandluse (ER) funktsiooni kasutatakse.
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
ms.openlocfilehash: ec4fdce6f072c5c3d87b139c8f64bd63a8a3eccd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855641"
---
# <a name="roundup-er-function"></a>ER-i funktsioon ROUNDUP

[!include [banner](../includes/banner.md)]

Funktsioon `ROUNDUP` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist ülespoole määratud arvu komakohtadeni.

## <a name="syntax"></a>Süntaks

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumendid

`number`: *tegelik*

Numbriline väärtus, mis tuleb ümardada ülespoole.

`decimals`: *täisarv*

Arvuline väärtus, mis tähistab kümnendkohtade arvu.

## <a name="return-values"></a>Tagastusväärtused

*Tegelik*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

See funktsioon toimib nagu [ROUND](er-functions-mathematical-round.md), kuid see ümardab alati määratud numbrit ülespoole (nullist kaugemale).

## <a name="example-1"></a>Näide 1

`ROUNDUP (1200.763, 2)` ümardab ülespoole kahe komakohani ja tagastab väärtuse **1200,77**.

## <a name="example-2"></a>Näide 2

`ROUNDUP (1200.767, -3)` ümardab ülespoole lähima 1000 kordseni ja tagastab väärtuse **2000**.

## <a name="additional-resources"></a>Lisaressursid

[Matemaatilised funktsioonid](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]