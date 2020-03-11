---
title: ER-i funktsioon AND
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni AND.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041810"
---
# <a name="AND">ER-i funktsioon AND</a>

[!include [banner](../includes/banner.md)]

Kui kõik määratud tingimused on tõesed, tagastab funktsioon `AND` *kahendmuutuja* väärtuse **TRUE**. Muidu tagastab see *kahendväärtuse* **VÄÄR**.

## <a name="syntax"></a>Süntaks

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumendid

`condition 1`: *kahendmuutuja*

Kehtiv tingimuslik avaldis, mida tuleb testida. See argument on kohustuslik.

`condition N`: *kahendmuutuja*

Kehtiv tingimuslik avaldis, mida tuleb testida. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*Kahendmuutuja*

Tulemiks saadud *kahendmuutuja* väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Loogiliste funktsioonide argumentides saate kasutada andmeallika viiteid, numbrilisi ja teksti väärtuseid, kahendmuutuja väärtusi, võrdluse tehtemärke ja teisi elektroonilise aruandluse (ER) funktsioone. Samas peavad kõik argumendid olema hinnatud *kahendmuutuja* väärtusele **TRUE** või **FALSE**.

## <a name="example"></a>Näide

`AND (1=1, "a"="a")` tagastab väärtuse **TRUE**.

`AND (1=2, "a"="a")` tagastab väärtuse **FALSE**.

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)
