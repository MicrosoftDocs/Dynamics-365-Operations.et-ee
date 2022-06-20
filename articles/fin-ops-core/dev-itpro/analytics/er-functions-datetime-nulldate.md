---
title: ER-i funktsioon NULLDATE
description: See artikkel annab teavet SELLE kohta, kuidas nulldate elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 7d1f0535796da096253dbd3ed55e9407cc9150f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870402"
---
# <a name="nulldate-er-function"></a>ER-i funktsioon NULLDATE

[!include [banner](../includes/banner.md)]

Funktsioon `NULLDATE` tagastab *kuupäeva* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuar 1900).

## <a name="syntax"></a>Süntaks

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Tagastusväärtused

*Kuupäev*

Tulemiks saadud kuupäeva väärtus.

## <a name="example-1"></a>Näide 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` tagastab kuupäeva **null** (1. jaanuar 1900) kujul **„1900-01-01”**, mis põhineb määratletud kohandatud vormingul.

## <a name="example-2"></a>Näide 2

Avaldis `IF( Invoice.DocumentDate = NULLDATE(), true, false)` tagastab väärtuse **tõene**, kui välja **DocumentDate** väärtus on võrdne kuupäevaga **null**. Selles näites on **Invoice** tüübi **Finance / tabeli kirjed** elektrilise aruandluse (ER) andmeallikas ja see viitab tabelile CustInvoiceJour.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]