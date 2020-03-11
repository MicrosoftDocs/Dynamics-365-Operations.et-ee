---
title: ER-i funktsioon FIRSTORNULL
description: Selles teemas selgitatakse, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FIRSTORNULL
author: NickSelin
manager: kfend
ms.date: 11/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86c8a0ae21ffeb6268efbbd198f7c709c2ad54f6
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042109"
---
# <a name="FIRSTORNULL">ER-i funktsioon FIRSTORNULL</a>

[!include [banner](../includes/banner.md)]

Funktsioon `FIRSTORNULL` tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see kirje pole tühi. Kui kirje on tühi, tagastab see funktsioon *konteineri (kirje)* väärtuse null.

## <a name="syntax"></a>Süntaks

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="example"></a>Näide

Avaldis `FIRSTORNULL(SPLIT("",1)).Value` tagastab tühja stringi (**„”**).

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)
