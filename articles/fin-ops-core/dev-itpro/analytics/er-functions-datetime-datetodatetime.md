---
title: ER-i funktsioon DATETODATETIME
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni DATETODATETIME Electronic Reporting (ER).
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
ms.openlocfilehash: 30fe75c7fd68edfff3e3778192723792d0f342ab
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287304"
---
# <a name="datetodatetime-er-function"></a>ER-i funktsioon DATETODATETIME

[!include [banner](../includes/banner.md)]

Funktsioon `DATETODATETIME` tagastab *kuupäeva ja kellaaja* väärtuse, mis teisendatakse määratud kuupäeva väärtusest kuupäeva/kellaaja väärtuseks koordineeritud maailmaajas (Greenwichi aeg \[GMT\]).

## <a name="syntax"></a>Süntaks

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumendid

`date`: *kuupäev*

Kuupäeva väärtus, mis tähistab teisendatavat kuupäeva.

## <a name="return-values"></a>Tagastusväärtused

*DateTime*

Tulemiks saadud kuupäeva/kellaaja väärtus.

## <a name="example-1"></a>Näide 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')`: tagastab Microsoft Dynamics praeguse 365 finantsseansi kuupäeva, 24. detsember 2015, **seisuga 24.01.242015 12:00:00**. Selles näites on **CompInfo** finantside ja toimingute/**tabeli tüübi elektronaruandluse (ER)** andmeallikas ja see viitab tabelile CompanyInfo.

## <a name="example-2"></a>Näide 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` tagastab kuupäeva/kellaaja väärtuse **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
