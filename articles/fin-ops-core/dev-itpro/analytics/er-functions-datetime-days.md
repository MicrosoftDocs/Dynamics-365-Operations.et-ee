---
title: ER-i funktsioon DAYS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DAYS
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47d992d061f8664a55332024ee5c6cd41e4bc495
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743563"
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
