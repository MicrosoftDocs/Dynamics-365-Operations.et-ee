---
title: ER-i funktsioon TEXT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TEXT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 20313133ce29b8d5048814ff78ce4ea4f5c54d4a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743684"
---
# <a name="text-er-function"></a>ER-i funktsioon TEXT

[!include [banner](../includes/banner.md)]

Funktsioon `TEXT` tagastab määratud arvu *stringi* väärtusena pärast seda, kui see on teisendatud tekstistringiks, mis on vormindatud praeguse rakenduse eksemplari serverilokaadi sätete kohaselt.

## <a name="syntax"></a>Süntaks

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumendid

`number`: *täisarv* või *tegelik*

Number, mis tuleb teisendada tekstistringiks.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Tüübi *Tõeline* väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.

## <a name="example"></a>Näide

Kui Microsoft Dynamics 365 Finance’i eksemplari serverilokaat on määratud kui **EN-US**, tagastab `TEXT (NOW ())` praeguse rakenduse Finance seansi kuupäeva 17. detsember 2015 tekstistringina **„12/17/2015 07:59:23 AM”**. `TEXT (1/3)` tagastab **„0,33”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)
