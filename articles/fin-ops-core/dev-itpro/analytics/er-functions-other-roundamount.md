---
title: ER-i funktsioon ROUNDAMOUNT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ROUNDAMOUNT.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: cce35a33ca179ad85bbde879122d3afbeefe5ee7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745659"
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

Kui parameeter `round rule` on seatud suvandile **RoundOffType.Ordinary**, käitub see funktsioon sarnaselt Exceli funktsioonile [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) ja X++ funktsioonile [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round).

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