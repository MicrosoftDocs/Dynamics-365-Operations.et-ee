---
title: ER-i funktsioon NULLDATE
description: See artikkel annab teavet SELLE kohta, kuidas nulldate elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 276ad99303a4e88ecb1c83e9518e06bfd7afaa45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272648"
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
