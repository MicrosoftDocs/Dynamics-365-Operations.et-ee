---
title: ER-i funktsioon VALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745509"
---
# <a name="value-er-function"></a>ER-i funktsioon VALUE

[!include [banner](../includes/banner.md)]

Funktsioon `VALUE` tagastab *tegeliku* väärtuse, mis konverteeritakse määratud stringist.

## <a name="syntax"></a>Süntaks

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Stringi väärtus, mis tuleb teisendada numbriliseks väärtuseks.

## <a name="return-values"></a>Tagastusväärtused

*Tegelik*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Komasid ja punkte (.), loetakse komakohtade eraldajateks ning miinusmärki (–) kasutatakse negatiivse märgina. Käitusajal esitatakse erand, kui määratud stringis on muid mittenumbrilisi märke.

## <a name="example-1"></a>Näide 1

`VALUE ("1 234,56")` annab erandi.

## <a name="example-2"></a>Näide 2

`VALUE ("1234,56")` tagastab **1234,56**.

## <a name="additional-resources"></a>Lisaressursid

[Tüübiteisenduse funktsioonid](er-functions-category-type-conversion.md)
