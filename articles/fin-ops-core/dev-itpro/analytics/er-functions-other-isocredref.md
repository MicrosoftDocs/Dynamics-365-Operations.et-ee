---
title: ER-i funktsioon ISOCREDREF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ISOCREDREF.
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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744091"
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
