---
title: ER-i funktsioon SPLITLIST
description: See artikkel annab teavet SELLE kohta, kuidas SPLITLIST elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 03/15/2021
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
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292522"
---
# <a name="splitlist-er-function"></a>ER-i funktsioon SPLITLIST

[!include [banner](../includes/banner.md)]

Funktsioon `SPLITLIST` jaotab määratud loendi alamloenditeks (või partiideks), millest igaüks sisaldab määratud kirjete arvu. See tagastab seejärel tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest.

## <a name="syntax-1"></a>Süntaks 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`number`: *täisarv*

Maksimaalne kirjete arv partii kohta.

`on-demand reading flag`: *kahendmuutuja*

*Loogiline* väärtus, mis täpsustab, kas alamloendi elemendid peaksid olema loodud nõudmisel.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Tagastatav partiide loend sisaldab järgmisi elemente.

 - **Väärtus:** *loend*

    Kirjete loend, mis kuuluvad praegusesse partiisse.

- **BatchNumber:** *täisarv*

    Praeguse partii number tagastatud loendis.

Kui nõudmisel lugemise lipp on seatud väärtusele **Tõene**, luuakse taotluse korral alamloendid, mis võimaldab mälutarbimise vähendamist, kuid võib põhjustada jõudluse hõivamise, kui elemente ei kasutata järjestikku.

## <a name="example"></a>Näide

Järgmisel joonisel luuakse andmeallikas **Read** kolme kirjet omava kirjete loendina. See loend on jaotatud partiideks, millest igaüks sisaldab kuni kahte kirjet.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Järgmisel joonisel on näidatud koostatud vormingu paigutus. Selles vormi paigutuses luuakse andmeallika **Read** sidemed, et luua XML-vormingus väljund. See väljund esitab üksikuid sõlmi igale partiile ja selles olevale kirjele.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
