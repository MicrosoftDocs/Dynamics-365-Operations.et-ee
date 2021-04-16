---
title: ER-i funktsioon WHERE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni WHERE.
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
ms.openlocfilehash: bdf5c658fda83399c7bcffeaaf07005164c53f8a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745493"
---
# <a name="where-er-function"></a>ER-i funktsioon WHERE

[!include [banner](../includes/banner.md)]

Funktsioon `WHERE` tagastab määratud loendi *kirjete loendi* väärtusena, kui see on vastavalt määratud tingimusele filtreeritud.

## <a name="syntax"></a>Süntaks

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`condition`: *kahendmuutuja*

Kehtiv tingimuslik avaldis, mida kasutatakse määratud loendi kirjete filtreerimiseks.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Erinevalt funktsioonist [FILTER](er-functions-list-filter.md) rakendatakse määratud tingimust kõigile tüübi *Kirjete loend* elektroonilise aruandluse (ER) andmeallikatele, mis asuvad mälus.

Kui argumendid, mis on selle funktsiooni jaoks konfigureeritud (`list` ja `condition`), võimaldavad selle taotluse otsesesse SQL-kutsesse tõlkida, esitatakse kujundamise ajal hoiatusteade. See sõnum teavitab kasutajat, et jõudlust võib parandada, kui funktsiooni `WHERE` asemel kasutatakse funktsiooni [FILTER](er-functions-list-filter.md).

## <a name="example-1"></a>Näide 1

Kui **Hankija** on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `WHERE (Vendors, Vendors.VendGroup = "40")` loendi ainult hankijatega, mis kuuluvad hankijate gruppi 40.

## <a name="example-2"></a>Näide 2

Kui sisestate andmeallika **DS** tüübile *Arvutatud väli* ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `WHERE( DS, DS.Value = "B")` loendi ainult ühe kirjega, mis sisaldab väljal **Väärtus** teksti **„B”**.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]