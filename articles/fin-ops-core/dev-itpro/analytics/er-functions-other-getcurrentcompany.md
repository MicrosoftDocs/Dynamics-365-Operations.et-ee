---
title: ER-i funktsioon GETCURRENTCOMPANY
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni GETCURRENTCOMPANY Electronic Reporting (ER).
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 06d552a0e8241d416fc49c4377b02f90fdf63d29
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872738"
---
# <a name="getcurrentcompany-er-function"></a>ER-i funktsioon GETCURRENTCOMPANY

[!include [banner](../includes/banner.md)]

Funktsioon `GETCURRENTCOMPANY` tagastab *stringi* väärtuse, mis tähistab juriidilise isiku (ettevõtte) koodi, kuhu kasutaja on praegu sisse loginud.

## <a name="syntax"></a>Süntaks

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example"></a>Näide

`GETCURRENTCOMPANY ()` tagastab **USMF**-i kasutaja puhul, kes on logitud sisse ettevõttesse **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]