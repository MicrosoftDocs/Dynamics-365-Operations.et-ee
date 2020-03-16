---
title: ER-i funktsioon IF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni IF.
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
ms.openlocfilehash: 198210f15e75de761dbb03e5087ba7c77a95721a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041741"
---
# <a name="IF">ER-i funktsioon IF</a>

[!include [banner](../includes/banner.md)]

Funktsioon `IF` annab vastuseks esimese määratud väärtuse, kui määratud tingimus on täidetud. Muul juhul annab see vastuseks teise määratud väärtuse. Tagastatav väärtus võib olla toetatud andmetüüpide mis tahes väärtus.

## <a name="syntax"></a>Süntaks

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumendid

`condition`: *kahendmuutuja*

Kehtiv tingimuslik avaldis, mida tuleb testida.

`first value`: *mis tahes toetatud andmetüüp*

Tagastatav tulemus, kui tingimus on täidetud.

`second value`: *mis tahes toetatud andmetüüp*

Tagastatav tulemus, kui tingimus ei ole täidetud.

## <a name="return-values"></a>Tagastusväärtused

*Mis tahes toetatud andmetüüp*

Mis tahes toetatud andmetüübi tulemuseks olev väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Argumendid `first value` ja `second value` tuleb määrata sama andmetüüpi kasutades. Kujundamise ajal esitatakse erand, kui konfigureeritud väärtuste andmetüübid ei ühti.

Kui esimene väärtus ja teine vöörtus on andmetüübi *Konteiner (kirje)* või *Kirjete loend* väärtused, on tulemuses ainult väljad, mis eksisteerivad mõlemas väärtuses.

## <a name="example"></a>Näide

`IF (1=2, "condition is met", "condition is not met")` tagastab stringi **„tingimus ei ole täidetud”**.

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)
