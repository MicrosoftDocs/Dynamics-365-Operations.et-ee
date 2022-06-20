---
title: ER-i funktsioon CHAR
description: See artikkel annab teavet CHAR-i elektroonilise aruandluse (ER) funktsiooni kohta.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1fb1d25c2624894e7bb0fa34b7bc48905a9289a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881486"
---
# <a name="char-er-function"></a>ER-i funktsioon CHAR

[!include [banner](../includes/banner.md)]

Funktsioon `CHAR` tagastab *stringi* väärtuse, mis kujutab üksikut märki, millele viitab määratud Unicode’i number.

## <a name="syntax"></a>Süntaks

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumendid

`number`: *täisarv*

Arv, mis vastab eeldatavale üksikule märgile.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Selle funktsiooni tagastatud string sõltub vormingu **FILE** ülemelemendis valitud kodeeringust. Toetatud kodeeringute loendi leiate teemast [Kodeeringuklass](/dotnet/api/system.text.encoding).

## <a name="example"></a>Näide

`CHAR (255)` tagastab **„ÿ”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]