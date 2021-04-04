---
title: Funktsioon ENDSWITH ER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse ENDSWITH elektroonilise aruandluse (ER) funktsiooni.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 2470bd8c75cf690d701957c4c79009659d61f7a5
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557511"
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

Seda funktsiooni saab kasutada [FILTRI](er-functions-list-filter.md) funktsiooni tingimuseavaldise määramiseks ainult siis, kui vastav vastendamine on konfigureeritud [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) juurdepääsuks [Microsoft Dataverse](../data-entities/data-integration-cds.md). Vastasel korral ilmneb erand kujundusajas. Teile kuvatav teade soovitab teil kasutada tõhususe parandamiseks funktsiooni [WHERE](er-functions-list-where.md) funktsiooni `FILTER` funktsiooni asemel.

## <a name="example-1"></a>Näide 1

Avaldis `ENDSWITH ("abc", "d")` tagastab **väär** väärtuse, samas kui avaldis `ENDSWITH ("abc", "C")` tagastab väärtuse **tõene**.

## <a name="example-2"></a>Näide 2

Avaldis `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` tagastab väärtuse **tõene** kui mudeli andmeallika **aadressi** välja **mudeli** andmeallikas lõpeb stringiga **USA**. Muidu tagastatakse väärtus **Väär**.

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)
