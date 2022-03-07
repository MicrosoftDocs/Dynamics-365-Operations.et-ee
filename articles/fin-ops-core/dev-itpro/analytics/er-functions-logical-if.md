---
title: ER-i funktsioon IF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni IF.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565900"
---
# <a name="if-er-function"></a>ER-i funktsioon IF

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]