---
title: ER-i funktsioon SESSIONNOW
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni SESSIONNOW Electronic Reporting (ER).
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
ms.openlocfilehash: 1cf092d55728f23cb10070324abc4458004946c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272618"
---
# <a name="sessionnow-er-function"></a>ER-i funktsioon SESSIONNOW

[!include [banner](../includes/banner.md)]

Funktsioon `SESSIONNOW` tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva ja kellaaega.

## <a name="syntax"></a>Süntaks

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>Tagastusväärtused

*DateTime*

Tulemiks saadud kuupäeva/kellaaja väärtus.

## <a name="example"></a>Näide

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24.12.2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
