---
title: ER-i funktsioon ADDDAYS
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni ADDDAYS Electronic Reporting (ER).
author: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 69273794def0dc52dc8e31615c319ccf5067fa77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274135"
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
