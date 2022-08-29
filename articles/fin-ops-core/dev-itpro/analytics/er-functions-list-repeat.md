---
title: KORDA ER-funktsiooni
description: See artikkel annab teavet selle kohta, kuidas kasutada korduse elektroonilise aruandluse (ER) funktsiooni.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220722"
---
# <a name="repeat-er-function"></a>KORDA ER-funktsiooni

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funktsioon `REPEAT` loob kirje, mis sisaldab välja, mille väärtus vastab määratud sisestusega. Seejärel tagastab see kirjeloendi *,* mida korratakse määratud arv kordi.

## <a name="syntax"></a>Süntaks

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumendid

`item`: iga toetatud [primitiivne või](er-formula-supported-data-types-primitive.md)[liitandmetüüp](er-formula-supported-data-types-composite.md)

Kordav väärtus.

`number`: *täisarv*

Korduste arv.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Tagastatud korduvate kirjete loend sisaldab järgmisi välju:

- Määratud väärtus (`Item` väli)
- Praeguse kirje indeks (`Number` väli)

> [!NOTE]
> Kuna selle funktsiooni puhul kasutatakse ühe põhinumbrit, `Number` on tulemuseks saadud **loendi esimese kirje väärtus 1**.

Seda funktsiooni saate [kasutada olemasolevate andmete korrutamiseks nii, et saate teha elektroonilise aruandluse (ER) lahenduste jõudlust ja mahu testimist Regression Suite’i automatiseerimistööriista (RSAT)](general-electronic-reporting.md)[abil](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Näide

Soovite luua dokumendi XML-vormingus, mis peab sisaldama nii palju XML-elemente `Party`, kui määrate käitusajal dialoogiboksi andmesisestusväljal, enne kui algab ER-vormingu käivitamine.

Järgmine joonis näitab ER-vormingut [...](er-overview-components.md#format-component). Selles vormingus lisatakse üksik `Party` XML-element, et seada ühe osapoole atribuudid.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Järgmine näide näitab järgmisi konfigureeritud andmeallikaid:

- Andmeallikas `Party`, mis esindab ühte osapoolt Seda `Party.Value` välja kasutatakse üksiku tekstiväärtuse näitamiseks.
- Andmeallikas `NumberOfRepeats`[...](er-user-input-parameter-data-sources.md), mida kasutatakse andmesisestusvälja pakkumiseks dialoogiaknas käitusajal, nii et saate määrata osapoolte arvu, kes tuleb loodud dokumenti sisestada.
- Andmeallikas `Party2`, mis kordab `Party` kirjet andmeallikas määratud kordade `NumberOfRepeats` arvu

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Järgmine näide näitab redigeeritava ER-vormingu andmete sidumisi, mis luuakse väljundi loomiseks XML-vormingus. See väljund esitatakse üksikutele osapooltele loetletud sõlmedeks.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Järgmine näide näitab tulemust, kui kujundatud vorming on käivitunud ja `NumberOfRepeats` andmeallika väärtus on määratud **5-na**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
