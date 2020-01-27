---
title: ER-i funktsioon GETENUMVALUEBYNAME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916840"
---
# <a name="GETENUMVALUEBYNAME">ER-i funktsioon GETENUMVALUEBYNAME</a>

[!include [banner](../includes/banner.md)]

Funktsioon `GETENUMVALUEBYNAME` otsib määratud *loetelu* andmeallikast konkreetset loetelu väärtust, kasutades loendi nime, mis on määratud *stringi* väärtuseks. Kui *loetelu* väärtus leitakse, tagastab funktsioon selle. Vastasel korral tagastab funktsioon loendamise väärtuse **null**.

## <a name="syntax"></a>Süntaks

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumendid

`enumeration data source path`: *loetelu*

Ühe järgmistest loenditüüpidest andmeallika kehtiv tee.

- Elektroonilise aruandluse (ER) mudeli loetelu
- ER-vormingu loetelu
- Microsoft Dynamics 365 Finance’i loetelu

`enumeration value text`: *string*

Stringi väärtus, mis tähistab ühe loetelu väärtuse nime.

## <a name="return-values"></a>Tagastusväärtused

Nullitav *loetelu*

Tulemiks saadud loetelu väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Ühtegi erandit ei esitata, kui väärtust *Loetelu* ei leita, kasutades loetelu väärtuse nime, mis on määratud *stringi* väärtuseks.

## <a name="example"></a>Näide

Järgmises näites on andmemudelis kasutusele võetud loetelu **ReportDirection**. Pange tähele, et loetelu väärtuste puhul on määratletud sildid.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Järgmises näites on toodud järgmised üksikasjad:

- Andmeallikas **$Direction** konfigureeritakse ER-i aruandes. See andmeallikas konfigureeritakse mudeli **ReportDirection** loetelu põhjal.
- Avaldis `$IsArrivals` on mõeldud kasutama mudeli loetelul põhinevat andmeallikat **$Direction** selle funktsiooni parameetrina.
- Võrdluse avaldise väärtus on **TRUE**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)
