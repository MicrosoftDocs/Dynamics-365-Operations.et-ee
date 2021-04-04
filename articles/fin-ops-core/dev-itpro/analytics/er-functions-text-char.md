---
title: ER-i funktsioon CHAR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CHAR.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: b008cf6ddf51d816a17e0fae1fa0db464adeabde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563194"
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

Selle funktsiooni tagastatud string sõltub vormingu **FILE** ülemelemendis valitud kodeeringust. Toetatud kodeeringute loendi leiate teemast [Kodeeringuklass](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Näide

`CHAR (255)` tagastab **„ÿ”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]