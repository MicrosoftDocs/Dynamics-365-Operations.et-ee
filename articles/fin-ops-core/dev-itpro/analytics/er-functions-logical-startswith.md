---
title: Funktsioon STARTSWITH ER
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni STARTSWITH Electronic reporting (ER).
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
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287214"
---
# <a name="startswith-er-function"></a>Funktsioon STARTSWITH ER

[!include [banner](../includes/banner.md)]

See `STARTSWITH` funktsioon määratleb, kas määratud sisestus algab määratud tekstiga. See toob *Tõeväärtus* väärtuseks **Tõde** määratud sisestusteksti, kui see algab määratud tekstiga. Muidu tagastab see *kahendväärtuse* **VÄÄR**.

## <a name="syntax"></a>Süntaks

```vb
STARTSWITH (input, start text)
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

Avaldis `STARTSWITH ("abc", "d")` tagastab **väär** väärtuse, samas kui avaldis `STARTSWITH ("abc", "A")` tagastab väärtuse **tõene**.

## <a name="example-2"></a>Näide 2

Avaldis `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` tagastab väärtuse **tõene** kui mudeli andmeallika **aadressi** välja **mudeli** andmeallikas algab stringiga, mis algab **123 Coffee Street**. Muidu tagastatakse väärtus **Väär**.

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)
