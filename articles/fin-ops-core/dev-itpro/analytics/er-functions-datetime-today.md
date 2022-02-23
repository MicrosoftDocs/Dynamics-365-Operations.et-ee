---
title: ER-i funktsioon TODAY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a93a9171456fb69e16c8104b0afb9ad485311b1a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683791"
---
# <a name="today-er-function"></a>ER-i funktsioon TODAY

[!include [banner](../includes/banner.md)]

Funktsioon `TODAY` tagastab *kuupäeva* väärtuse, mis tähistab rakendusserveri praegust kuupäeva.

## <a name="syntax"></a>Süntaks

```xpp
TODAY ()
```

## <a name="return-values"></a>Tagastusväärtused

*Kuupäev*

Tulemiks saadud kuupäeva väärtus.

## <a name="example"></a>Näide

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` tagastab praeguse rakendusserveri kuupäeva väärtuse 24. detsember 2015 stringi kujul **„24-12-2015”** määratud kohandatud vormingu kohaselt.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)
