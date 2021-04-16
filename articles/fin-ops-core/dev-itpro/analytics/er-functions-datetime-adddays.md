---
title: ER-i funktsioon ADDDAYS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ADDDAYS.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 0c420daa04b8e22504d25d317c75826f1d1914b7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747055"
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