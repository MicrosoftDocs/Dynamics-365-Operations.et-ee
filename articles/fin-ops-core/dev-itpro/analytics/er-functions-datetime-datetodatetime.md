---
title: ER-i funktsioon DATETODATETIME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATETODATETIME.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 961ccd18e70d4f9851027492366a7d9408a668c5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042408"
---
# <a name="DATETODATETIME">ER-i funktsioon DATETODATETIME</a>

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

`DATETODATETIME (CompInfo. 'getCurrentDate()')` tagastab jooksva Dynamics 365 Finance’i seansi 24. detsembril 2015 kujul **12/24/2015 12:00:00 AM**. Selles näites on **CompInfo** tüübi **Finance and Operations / tabel** elektroonilise aruandluse (ER) andmeallikas ja see viitab tabelile CompanyInfo.

## <a name="example-2"></a>Näide 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` tagastab kuupäeva/kellaaja väärtuse **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)
