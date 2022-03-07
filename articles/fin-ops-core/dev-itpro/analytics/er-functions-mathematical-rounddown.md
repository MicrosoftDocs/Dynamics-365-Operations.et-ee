---
title: ER-i funktsioon ROUNDDOWN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ROUNDDOWN.
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
ms.openlocfilehash: 77186dc4d607f419149e4001a7404afba9e80fc7ec2528b840261a329a1e7872
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747293"
---
# <a name="rounddown-er-function"></a>ER-i funktsioon ROUNDDOWN

[!include [banner](../includes/banner.md)]

Funktsioon `ROUNDDOWN` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist allapoole määratud arvu komakohtadeni.

## <a name="syntax"></a>Süntaks

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumendid

`number`: *tegelik*

Numbriline väärtus, mis tuleb ümardada allapoole.

`decimals`: *täisarv*

Arvuline väärtus, mis tähistab kümnendkohtade arvu.

## <a name="return-values"></a>Tagastusväärtused

*Tegelik*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

See funktsioon toimib nagu [ROUND](er-functions-mathematical-round.md), kuid see ümardab alati määratud numbrit allapoole (nulli poole).

## <a name="example-1"></a>Näide 1

`ROUNDDOWN (1200.767, 2)` ümardab allapoole kahe komakohani ja tagastab väärtuse **1200,76**. 

## <a name="example-2"></a>Näide 2

`ROUNDDOWN (1700.767, -3)` ümardab allapoole lähima 1000 kordseni ja tagastab väärtuse **1000**.

## <a name="additional-resources"></a>Lisaressursid

[Matemaatilised funktsioonid](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]