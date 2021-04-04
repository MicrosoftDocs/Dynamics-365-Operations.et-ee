---
title: ER-i funktsioon ISOCREDREF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ISOCREDREF.
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
ms.openlocfilehash: a9378028a4b308aae7796b861b37a5f89ddfe49c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563402"
---
# <a name="isocredref-er-function"></a>ER-i funktsioon ISOCREDREF

[!include [banner](../includes/banner.md)]

Funktsioon `ISOCREDREF` tagastab *stringi* väärtuse, mis tähistab Rahvusvahelise Standardiorganisatsiooni (ISO) kreeditori viidet määratud arve numbri arvude ja tähestikus olevate sümbolite alusel.

## <a name="syntax"></a>Süntaks

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumendid

`invoice number digits`: *string*

Teksti väärtus, mis tähistab arve numbri numbreid.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

> [!NOTE] 
> ISO-ga ühildumatute sümbolite tähestikust eemaldamiseks tuleb argument `invoice number digits` enne sellele funktsioonile edastamist tõlkida.

## <a name="example"></a>Näide

`ISOCredRef ("VEND-200002")` tagastab **„RF23VEND-200002”**.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]