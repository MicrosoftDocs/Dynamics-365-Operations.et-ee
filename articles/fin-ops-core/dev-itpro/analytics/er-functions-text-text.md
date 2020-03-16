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
ms.openlocfilehash: c08aca949ffc7e62009bf3f6c664d96b368f43e7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040890"
---
# <a name="TEXT">ER-i funktsioon TEXT</a>

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
