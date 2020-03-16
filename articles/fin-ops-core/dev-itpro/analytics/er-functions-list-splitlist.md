---
title: ER-i funktsioon SPLITLIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLITLIST.
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
ms.openlocfilehash: 56ef02e3ea0ca2207ccdc79468a9ea4c1fbe8f95
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041879"
---
# <a name="SPLITLIST">ER-i funktsioon SPLITLIST</a>

[!include [banner](../includes/banner.md)]

Funktsioon `SPLITLIST` jaotab määratud loendi alamloenditeks (või partiideks), millest igaüks sisaldab määratud kirjete arvu. See tagastab seejärel tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest.

## <a name="syntax"></a>Süntaks

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`number`: *täisarv*

Maksimaalne kirjete arv partii kohta.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Tagastatav partiide loend sisaldab järgmisi elemente.

 - **Väärtus:** *loend*

    Kirjete loend, mis kuuluvad praegusesse partiisse.

- **BatchNumber:** *täisarv*

    Praeguse partii number tagastatud loendis.

## <a name="example"></a>Näide

Järgmisel joonisel luuakse andmeallikas **Read** kolme kirjet omava kirjete loendina. See loend on jaotatud partiideks, millest igaüks sisaldab kuni kahte kirjet.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Järgmisel joonisel on näidatud koostatud vormingu paigutus. Selles vormi paigutuses luuakse andmeallika **Read** sidemed, et luua XML-vormingus väljund. See väljund esitab üksikuid sõlmi igale partiile ja selles olevale kirjele.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)
