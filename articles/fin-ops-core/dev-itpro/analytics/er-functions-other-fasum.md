---
title: ER-i funktsioon FA_SUM
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FA_SUM.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 03bed091350b39601edb22b5af6bda5a83af47eb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041350"
---
# <a name="FA_SUM">ER-i funktsioon FA_SUM</a>

[!include [banner](../includes/banner.md)]

Funktsioon `FA_SUM` tagastab *konteineri (kirje)* väärtuse, mis koosneb põhivara summade andmetest määratud põhivara kauba, väärtusmudeli koodi ja kuupäevade perioodi kohta.

## <a name="syntax"></a>Süntaks

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumendid

`fixed asset code`: *string*

*Stringi* väärtus, mis tähistab põhivara kauba koodi, mille jaoks saldo arvutatakse.

`value model code`: *string*

*Stringi* väärtus, mis tähistab väärtusmudeli koodi, mille jaoks saldo arvutatakse.

`start date`: *kuupäev*

*Kuupäeva* väärtus, mis tähistab selle perioodi alguskuupäeva, mille kohta põhivara summad arvutatakse.

`end date`: *kuupäev*

*Kuupäeva* väärtus, mis tähistab selle perioodi lõpukuupäeva, mille kohta põhivara summad arvutatakse.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="example"></a>Näide

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` tagastab põhivara **COMP-000001** andmekonteineri,m mis on valmistatud ette väärtuse mudelile **Praegune** ja ajavahemikule alates **Date1** kuni **Date2**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)
