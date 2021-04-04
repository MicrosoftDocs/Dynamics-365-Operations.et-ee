---
title: ER-i funktsioon FA_BALANCE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FA_BALANCE.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: 37c440a5c626016ebdb75703a2be63c9a1a2b560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567588"
---
# <a name="fa_balance-er-function"></a>ER-i funktsioon FA_BALANCE

[!include [banner](../includes/banner.md)]

Funktsioon `FA_BALANCE` tagastab *konteineri (kirje)* väärtuse, mis koosneb põhivara saldo andmetest määratud põhivara kauba, väärtusmudeli koodi, aruandeaasta ja aruandluse kuupäeva kohta.

## <a name="syntax"></a>Süntaks

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumendid

`fixed asset code`: *string*

*Stringi* väärtus, mis tähistab põhivara kauba koodi, mille jaoks saldo arvutatakse.

`value model code`: *string*

*Stringi* väärtus, mis tähistab väärtusmudeli koodi, mille jaoks saldo arvutatakse.

`reporting year`: *loetelu väärtus*

Rakenduse loetelu **AssetYear** loendamise väärtus, mis määratleb saldo arvutamise perioodi.

`reporting date`: *kuupäev*

*Kuupäeva* väärtus, mis määratleb saldo arvutamise kuupäeva.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner (kirje)*

Tulemuseks olev kirje väärtus.

## <a name="example"></a>Näide

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` annab vastuseks põhivara **COMP-000001** väärtusmudeli **Praegune** jaoks ette valmistatud saldode andmekonteineri praegusel rakenduse seansi kuupäeval.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]