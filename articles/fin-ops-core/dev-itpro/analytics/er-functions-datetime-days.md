---
title: ER-i funktsioon DAYS
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni DAYS Electronic Reporting (ER).
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: a0c50e36bbf0c2bd999a17631e3e00d2feb162fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268721"
---
# <a name="days-er-function"></a>ER-i funktsioon DAYS

[!include [banner](../includes/banner.md)]

Funktsioon `DAYS` tagastab *täisarvu* väärtuse, mis tähistab ühe määratud kuupäeva ja teise määratud kuupäeva vahelise päevade arvu täisarvuna.

## <a name="syntax"></a>Süntaks

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumendid

`date 1`: *kuupäev*

Kuupäeva väärtus, mis tähistab päevade arvu arvutamiseks kasutatavat alguskuupäeva

`date 2`: *kuupäev*

Kuupäeva väärtus, mis tähistab päevade arvu arvutamiseks kasutatavat lõpukuupäeva

## <a name="return-values"></a>Tagastusväärtused

*Täisarv*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Funktsioon `DAYS` tagastab vastuseks positiivse väärtuse, kui esimene kuupäev on hilisem kui teine kuupäev, see tagastab väärtuse **0 (null)**, kui esimene kuupäev võrdub teise kuupäevaga, ja see tagastab vastuseks negatiivse väärtuse, kui esimene kuupäev on varasem kui teine kuupäev.

## <a name="example"></a>Näide

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` tagastab **–1**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
