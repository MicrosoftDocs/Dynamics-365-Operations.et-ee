---
title: ER-i funktsioon ENUMERATE
description: See artikkel annab teavet selle kohta, kuidas ENUMERATE elektroonilise aruandluse (ER) funktsiooni kasutatakse.
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
ms.openlocfilehash: adaa2582e6dced428cf1f15a235ecbfd036362e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273244"
---
# <a name="enumerate-er-function"></a>ER-i funktsioon ENUMERATE

[!include [banner](../includes/banner.md)]

Funktsioon `ENUMERATE` tagastab uue *kirjete loendi* väärtuse, mis koosneb määratud loendi nummerdatud kirjetest.

## <a name="syntax"></a>Süntaks

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Tagastatav nummerdatud kirjete loend näitab järgmisi täiendavaid elemente.

- Väljade kirje(komponent **Väärtus**)
- Praegune kirje indeks (komponent **Number**)

## <a name="example"></a>Näide

Järgmises näites on andmeallikas **Nummerdatud** loodud andmeallika **Hankijad hankijate** kirjete nummerdatud loendina, mis viitab tabelile VendTable.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Järgmine joonis näitab elektroonilise aruandluse (ER) vormingut. Selles vormingus luuakse andmesidemed, et luua XML-vormingus väljund. Selle väljund esitab üksikuid hankijaid nummerdatud sõlmedena.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
