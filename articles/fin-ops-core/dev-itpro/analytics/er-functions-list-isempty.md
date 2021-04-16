---
title: ER-i funktsioon ISEMPTY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ISEMPTY.
author: NickSelin
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750432"
---
# <a name="isempty-er-function"></a>ER-i funktsioon ISEMPTY

[!include [banner](../includes/banner.md)]

Kui määratud loend ei sisalda ühtegi kirjet, tagastab funktsioon `ISEMPTY` *kahendmuutuja* väärtuse **TRUE**. Muidu tagastab see *kahendväärtuse* **VÄÄR**.

## <a name="syntax"></a>Süntaks

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Kahendmuutuja*

Tulemiks saadud *kahendmuutuja* väärtus.

## <a name="example-1"></a>Näide 1

Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `ISEMPTY(DS)` väärtuse **FALSE**.

## <a name="example-2"></a>Näide 2

Avaldis `ISEMPTY (SPLIT ("",1))` tagastab väärtuse **TRUE**.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]