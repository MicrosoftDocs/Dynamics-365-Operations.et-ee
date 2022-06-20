---
title: ER-i funktsioon VALUE
description: See artikkel annab teavet selle kohta, kuidas kasutatakse väärtuse elektroonilise aruandluse (ER) funktsiooni.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: e96d274962ad79969a3158f7e352d3c72bd4072c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892976"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]