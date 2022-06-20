---
title: ER-i funktsioon FIRST
description: See artikkel annab teavet selle kohta, kuidas kasutatakse FIRST Electronic Reporting (ER) funktsiooni.
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
ms.openlocfilehash: a1f841fe11f025be95ffee2750da74ad7be51624
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906572"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]