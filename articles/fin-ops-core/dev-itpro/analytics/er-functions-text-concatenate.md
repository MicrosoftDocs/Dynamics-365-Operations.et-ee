---
title: ER-i funktsioon CONCATENATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CONCATENATE
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
ms.openlocfilehash: 1507e1b8a31ed45e7c540e4e2ff31b79e8de3b866ffbace9de17d7b3e169e877
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762496"
---
# <a name="concatenate-er-function"></a>ER-i funktsioon CONCATENATE

[!include [banner](../includes/banner.md)]

Funktsioon `CONCATENATE` tagastab kõik määratud tekstistringi *stringi* väärtusena pärast nende üheks stringiks ühendamist.

## <a name="syntax"></a>Süntaks

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumendid

`text 1`: *string*

Viide andmetüübi *String* andmeallikale. See argument on kohustuslik.

`text N`: *string*

Viide andmetüübi *String* andmeallikale. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`CONCATENATE ("abc", "def")` tagastab **„abcdef”**.

## <a name="usage-notes"></a>Kasutamise märkused

Avaldis `"abc" & "def"` annab vastuseks samuti väärtuse **„abcdef”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]