---
title: ER-i funktsioon NULLCONTAINER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NULLCONTAINER.
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
ms.openlocfilehash: ea71bfc4b30164fd32e804bf83a46c49cd18d155
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041465"
---
# <a name="NULLCONTAINER">ER-i funktsioon NULLCONTAINER</a>

[!include [banner](../includes/banner.md)]

Funktsioon `NULLCONTAINER` tagastab *konteineri (kirje)* väärtuse null, millel on sama struktuur, kui määratud kirjete loendil või kirjel.

## <a name="syntax"></a>Süntaks

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend* või *konteiner (kirje)*

Tüübi *Kirjete loend* või *Konteiner (kirje)* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

> [!NOTE] 
> See funktsioon on aegunud. Kasutage selle asemel funktsiooni `EMPTYRECORD`. Lisateavet vt [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Näide

`NULLCONTAINER (SPLIT ("abc", 1))` tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon `SPLIT`. Lisateavet vt [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Lisaressursid

[Kirje funktsioonid](er-functions-category-record.md)
