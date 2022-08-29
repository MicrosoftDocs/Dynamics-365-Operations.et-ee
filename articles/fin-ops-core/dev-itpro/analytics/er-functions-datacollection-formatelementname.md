---
title: ER-i funktsioon FORMATELEMENTNAME
description: See artikkel annab teavet selle kohta, kuidas formatELEMENTNAME elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 1c8c319075f8f39bec963df2c88d2d8d3beace43
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275421"
---
# <a name="formatelementname-er-function"></a>ER-i funktsioon FORMATELEMENTNAME

[!include [banner](../includes/banner.md)]

Funktsioon `FORMATELEMENTNAME` tagastab *stringi* väärtuse, mis tähistab praeguse elektroonilise aruandluse (ER) vormingu elemendi nime.

## <a name="syntax"></a>Süntaks

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Seda funktsiooni saab kutsuda ER-i avaldistes, mis konfigureeriti atribuutidele **Kogutud andmete võtme nimi** ja **Kogutud andmete võtme väärtus** ER-vormingu komponendile rühmast **Tekst**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.

## <a name="example"></a>Näide

Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest [ER-i loendamise ja liitmise vormingu väljundi kasutusandmed](tasks/er-format-counting-summing-1.md), mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa.

## <a name="additional-resources"></a>Lisaressursid

[Andmete kogumise funktsioonid](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
