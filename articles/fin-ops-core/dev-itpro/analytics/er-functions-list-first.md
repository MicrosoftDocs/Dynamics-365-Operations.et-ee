---
title: ER-i funktsioon FIRST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FIRST.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679410"
---
# <a name="first-er-function"></a>ER-i funktsioon FIRST

[!include [banner](../includes/banner.md)]

Funktsioon `FIRST` tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see loend pole tühi. Kui loend on tühi, esitab see funktsioon erandi.

## <a name="syntax"></a>Süntaks

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="example-1"></a>Näide 1

Avaldis `FIRST(SPLIT("ABC",1)).Value` tagastab tekstiväärtuse **„A”**.

## <a name="example-2"></a>Näide 2

Avaldis `FIRST(SPLIT("",1)).Value` tagastab käitusaja erandi.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)
