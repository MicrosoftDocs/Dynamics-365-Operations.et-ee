---
title: ER-i funktsioon CONVERTCURRENCY
description: See artikkel annab teavet CONVERTCURRENCY elektroonilise aruandluse (ER) funktsiooni kohta.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: ac9a1cbb1c0a4b381a4e268f563c6ab0dd9c8053
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275508"
---
# <a name="convertcurrency-er-function"></a>ER-i funktsioon CONVERTCURRENCY

[!include [banner](../includes/banner.md)]

Funktsioon `CONVERTCURRENCY` tagastab *tegeliku* väärtuse, mis kajastab määratud rahasumma määratud lähtevaluutast määratud sihtvaluutaks konverteerimise tulemust, kasutades määratud kuupäeval määratud ettevõtte sätteid.

## <a name="syntax"></a>Süntaks

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumendid

`amount`: *täisarv* või *tegelik*

Numbriline väärtus, mis tähistab rahasummat, mis tuleb teisendada.

`source currency`: *string*

Lähtevaluuta kood.

`target currency`: *string*

Sihtvaluuta kood.

`date`: *kuupäev*

*Kuupäeva* väärtus, mis tähistab kuupäeva, mida kasutatakse teisendamise vahetuskursi määramiseks.

`company`: *string*

*Stringi* väärtus, mis tähistab ettevõtte koodi, mis varustab teisenduseks kasutatavate sätetega.

## <a name="return-values"></a>Tagastusväärtused

*Tegelik*

Tulemiks saadud numbriline väärtus.

## <a name="example"></a>Näide

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` tagastab ühe euroga võrdse väärtuse USA dollarites praeguse seansi kuupäeval **DEMF**-i ettevõtte sätete alusel.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
