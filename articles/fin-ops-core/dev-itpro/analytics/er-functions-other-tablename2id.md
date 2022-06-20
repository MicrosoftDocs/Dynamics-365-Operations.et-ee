---
title: ER-i funktsioon TABLENAME2ID
description: See artikkel annab teavet selle kohta, kuidas TABELINAME2ID elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: b5deea69d5c43be599ccf02c0344ba8d662a6e0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886845"
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