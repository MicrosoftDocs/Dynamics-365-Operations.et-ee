---
title: ER-i funktsioon ADDDAYS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ADDDAYS.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 8877bf5a1b6c06e1a25fa9ddaca9c3b039bd2e4d01f39eea9065125977f73e9a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740331"
---
# <a name="adddays-er-function"></a>ER-i funktsioon ADDDAYS

[!include [banner](../includes/banner.md)]

Funktsioon `ADDDAYS` arvutab *kuupäeva ja kellaaja* väärtuse, mis on määratud alguskuupäevast varasemate või hilisemate päevade arv.

## <a name="syntax"></a>Süntaks

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumendid

`datetime`: *kuupäev ja kellaaeg*

Kuupäeva/kellaaja väärtus, mis tähistab alguskuupäeva.

`days`: *täisarv*

Päevade arv enne või pärast väärtust `datetime`.

## <a name="return-values"></a>Tagastusväärtused

*DateTime*

Tulemiks saadud kuupäeva/kellaaja väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Suvandi `days` positiivne väärtus annab tulemuseks kuupäeva tulevikus. Negatiivne väärtus annab kuupäeva minevikus.

## <a name="example-1"></a>Näide 1

`ADDDAYS (NOW(), 7)` tagastab kuupäeva ja kellaaja seitsme päeva pärast.

## <a name="example-2"></a>Näide 2

`ADDDAYS (NOW(), -3)` tagastab kuupäeva ja kellaaja kolme päeva eest.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]