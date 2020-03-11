---
title: ER-i funktsioon DAYOFYEAR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DAYOFYEAR.
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070663"
---
# <a name="DAYOFYEAR">ER-i funktsioon DAYOFYEAR</a>

[!include [banner](../includes/banner.md)]

Funktsioon `DAYOFYEAR` tagastab *täisarvu* väärtuse, mis tähistab 1. jaanuari ja määratud kuupäeva vahelise päevade arvu täisarvuna.

## <a name="syntax"></a>Süntaks

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumendid

`date`: *kuupäev*

Kuupäeva väärtus, mis tähistab päevade arvu arvutamiseks kasutatavat kuupäeva

## <a name="return-values"></a>Tagastusväärtused

*Täisarv*

Tulemiks saadud numbriline väärtus.

## <a name="example-1"></a>Näide 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` tagastab **61**.

## <a name="example-2"></a>Näide 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` tagastab **1**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)
