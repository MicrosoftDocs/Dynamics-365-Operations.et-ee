---
title: Funktsioon ENDSWITH ER
description: See artikkel annab teavet selle kohta, kuidas ENDSWITH elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 2608593238e5b2f738b452fb042837238f17e44e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271609"
---
# <a name="endswith-er-function"></a>Funktsioon ENDSWITH ER

[!include [banner](../includes/banner.md)]

See `ENDSWITH` funktsioon määratleb, kas määratud sisestus algab määratud tekstiga. See toob *Tõeväärtus* väärtuseks **Tõde** määratud sisestusteksti, kui see algab määratud tekstiga. Muidu tagastab see *kahendväärtuse* **VÄÄR**.

## <a name="syntax"></a>Süntaks

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Argumendid

`input`: *string*

Andmeallika kehtiv üksuse tee *Stringi* tüüpi või stringikonstandi, mille väärtus võib algata teise argumendiga.

`start text`: *string*

Andmeallika kehtiv üksuse tee *Stringi* tüüpi või stringikonstandi, mille väärtus võib algata teise argumendiga.

## <a name="return-values"></a>Tagastusväärtused

*Loogiline*

Tulemiks saadud *kahendmuutuja* väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Seda funktsiooni saab kasutada [FILTRI](er-functions-list-filter.md) funktsiooni tingimuseavaldise määramiseks ainult siis, kui vastav vastendamine on konfigureeritud [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) juurdepääsuks [Microsoft Dataverse](/power-platform/admin/data-integrator). Vastasel korral ilmneb erand kujundusajas. Teile kuvatav teade soovitab teil kasutada tõhususe parandamiseks funktsiooni [WHERE](er-functions-list-where.md) funktsiooni `FILTER` funktsiooni asemel.

## <a name="example-1"></a>Näide 1

Avaldis `ENDSWITH ("abc", "d")` tagastab **väär** väärtuse, samas kui avaldis `ENDSWITH ("abc", "C")` tagastab väärtuse **tõene**.

## <a name="example-2"></a>Näide 2

Avaldis `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` tagastab väärtuse **tõene** kui mudeli andmeallika **aadressi** välja **mudeli** andmeallikas lõpeb stringiga **USA**. Muidu tagastatakse väärtus **Väär**.

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)
