---
title: ER-i funktsioon REVERSE
description: See artikkel annab teavet SELLE kohta, kuidas kasutatakse PÖÖRD elektroonilise aruandluse (ER) funktsiooni.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 360878319bfa29395ae5deabec2e25e52d9e0fdc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284144"
---
# <a name="reverse-er-function"></a>ER-i funktsioon REVERSE

[!include [banner](../includes/banner.md)]

Funktsioon `REVERSE` tagastab määratud loendi *kirjete loendi* väärtusena pööratud sortimisjärjestuses.

## <a name="syntax"></a>Süntaks

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="example-1"></a>Näide 1

Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("C|B|A", "|")`, tagastab avaldis `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` teksti väärtuse **„C”**.

## <a name="example-2"></a>Näide 2

Kui **Hankija** on konfigureeritud elektroonilise aruandluse (ER) andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` hankijate loendi, mis on sorditud nimede järgi kahanevas järjestuses.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
