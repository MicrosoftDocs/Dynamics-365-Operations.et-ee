---
title: ER-i funktsioon TABLENAME2ID
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TABLENAME2ID.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d9f9e38f46df8a93b5cb16b8d0d5e5afbff8558a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743995"
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

Selle funktsiooni käitamisel võivad teenuse Microsoft Dynamics 365 Finance erinevatel eksemplaridel olla erinevad tulemused, isegi kui kasutatakse sama ettevõtte nime.

## <a name="example"></a>Näide

`TABLENAME2ID ("Intrastat")` tagastab **1510**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)
