---
title: ER-i funktsioon ENUMERATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ENUMERATE.
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
ms.openlocfilehash: f0a1c83ee869810e816b6d32ea890d172d2910e5
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916219"
---
# <a name="ENUMERATE">ER-i funktsioon ENUMERATE</a>

[!include [banner](../includes/banner.md)]

Funktsioon `ENUMERATE` tagastab uue *kirjete loendi* väärtuse, mis koosneb määratud loendi nummerdatud kirjetest.

## <a name="syntax"></a>Süntaks

```
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
