---
title: ER-i funktsioon TABLENAME2ID
description: See artikkel annab teavet selle kohta, kuidas TABELINAME2ID elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: fe7ed336f2264e15e0a8a7305e1bcebb75b2cd07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268052"
---
# <a name="tablename2id-er-function"></a>ER-i funktsioon TABLENAME2ID

[!include [banner](../includes/banner.md)]

Funktsioon `TABLENAME2ID` tagastab määratud tabeli nime tabeli ID numbrilise esituse *täisarvulise* väärtusena.

## <a name="syntax"></a>Süntaks

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Teksti väärtus, mis tähistab kehtivat tabeli nime.

## <a name="return-values"></a>Tagastusväärtused

*Täisarv*

Tulemiks saadud numbriline väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Selle funktsiooni käivitamine võib Microsoft Dynamics 365 Finantside eri eksemplarides olla erinev, isegi kui kasutatakse sama ettevõtte nime.

## <a name="example"></a>Näide

`TABLENAME2ID ("Intrastat")` tagastab **1510**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
