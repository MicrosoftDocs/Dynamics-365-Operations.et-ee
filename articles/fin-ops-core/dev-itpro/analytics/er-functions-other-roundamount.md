---
title: ER-i funktsioon ROUNDAMOUNT
description: See artikkel annab teavet selle kohta, kuidas ümardamise elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0e4de43f865ca21822ab2c0c345026d2e9113ca2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286025"
---
# <a name="roundamount-er-function"></a>ER-i funktsioon ROUNDAMOUNT

[!include [banner](../includes/banner.md)]

Funktsioon `ROUNDAMOUNT` tagastab määratud arvu määratud ümardamisreegli kohaselt lähima teise arvu kordseni ümardamise tulemusena *tegeliku* väärtuse.

## <a name="syntax"></a>Süntaks

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Argumendid

`number`: *täisarv* või *tegelik*

Numbriline väärtus, mis tuleb ümardada.

`decimals`: *täisarv* või *tegelik*

Arv, mida parameetri `number` väärtus peab kordseni ümardama.

`round rule`: *loetelu väärtus*

Loetelu **RoundOffType** loendamise väärtus, mis määratleb ümardamise reegli. See loendamine pakub järgmisi väärtusi.

- Tavaline (Ordinary)
- Allapoole (RoundDown)
- Ümardamine üles (RoundUp)

## <a name="return-values"></a>Tagastusväärtused

*Tegelik*

Tulemuseks olev arvväärtus on parameetri `decimals` määratud väärtuse korrutis ja on kõige lähemal parameetri `number` määratud väärtusele.

## <a name="usage-notes"></a>Kasutamise märkused

Kui parameeter `number` on null, tagastab funktsioon alati nulli.

Kui parameeter `decimals` on null, ümardab see funktsioon vaikimisi ümardamisväärtuseni. Kui parameeter `round rule` on seatud suvandile **RoundOffType.Ordinary**, on ümardamise vaikeväärtus **0,01.** Vastasel juhul on ümardamise vaikeväärtus **1,0**.

Kui parameeter `round rule` on seatud suvandile **RoundOffType.Ordinary**, ümardab see funktsioon lähima ümardatud summani.

Kui parameeter `round rule` on seatud suvandile **RoundOffType.RoundDown**, ümardab see funktsioon nulli suunas lähima ümardatud summani.

Kui parameeter `round rule` on seatud suvandile **RoundOffType.RoundUp**, ümardab see funktsioon nullist eemale lähima ümardatud summani.

Kui parameeter `round rule` on seatud suvandile **RoundOffType.Ordinary**, käitub see funktsioon sarnaselt Exceli funktsioonile [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) ja X++ funktsioonile [ROUND](../dev-ref/xpp-math-run-time-functions.md#round).

## <a name="remarks"></a>Märkused

Arvväärtuse ümardamiseks määratud arvu kümnendkohani kasutage funktsiooni [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>Näide

Kui parameeter **model.RoundOff** on seatud suvandile **RoundOffType.Ordinary**, tagastab `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` väärtuse 7,35. 

Kui parameeter **model.RoundOff** on seatud suvandile **RoundOffType.RoundDown**, tagastab `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` väärtuse 7,35. 

Kui parameeter **model.RoundOff** on seatud suvandile **RoundOffType.RoundUp**, tagastab `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` väärtuse 8,4.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)

[Matemaatilised funktsioonid](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
