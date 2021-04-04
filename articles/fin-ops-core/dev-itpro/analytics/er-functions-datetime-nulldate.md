---
title: ER-i funktsioon NULLDATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NULLDATE.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563458"
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