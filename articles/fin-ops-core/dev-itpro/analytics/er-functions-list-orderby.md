---
title: ER-i funktsioon ORDERBY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ORDERBY.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c39700fab90265ed1915b4815a6bb27af58d9516
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686460"
---
# <a name="orderby-er-function"></a>ER-i funktsioon ORDERBY

[!include [banner](../includes/banner.md)]

Funktsioon `ORDERBY` tagastab määratud loendi *kirjete loendi* väärtusena, kui see on vastavalt määratud argumentidele sorditud. Neid argumente saab määratleda avaldistena.

## <a name="syntax"></a>Süntaks

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`expression 1`: *väli*

Andmeallika välja kehtiv tee, millele viitab kutsutud funktsiooni argument `list`. Viidatud väli peab olema primitiivse andmetüübi väli. See argument on kohustuslik.

`expression N`: *väli*

Andmeallika välja kehtiv tee, millele viitab kutsutud funktsiooni argument `list`. Viidatud väli peab olema primitiivse andmetüübi väli. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="example-1"></a>Näide 1

Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("C|B|A", "|")`, tagastab avaldis `FIRST( ORDERBY( DS, DS. Value)).Value` teksti väärtuse **„A”**.

## <a name="example-2"></a>Näide 2

Kui **Hankija** on konfigureeritud elektroonilise aruandluse (ER) andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `ORDERBY (Vendors, Vendors.'name()')` hankijate loendi, mis on sorditud nimede järgi kasvavas järjestuses.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)
