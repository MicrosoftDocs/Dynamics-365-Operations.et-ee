---
title: ER-i funktsioon QRCODE
description: See artikkel annab teavet selle kohta, kuidas QRCODE elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 9de62eefb82942ccc72e81bd9bf36eed07c99dba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287184"
---
# <a name="qrcode-er-function"></a>ER-i funktsioon QRCODE

[!include [banner](../includes/banner.md)]

Funktsioon `QRCODE` tagastab *konteineri* väärtuse, mis esitab määratud stringi puhul binaarvormingus ruutkoodi (QR-koodi) pildi.

## <a name="syntax"></a>Süntaks

```vb
QRCODE (text)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

*Stringi* väärtus, mis tähistab algteksti.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner*

Tulemuseks olev binaarne voog.

## <a name="example"></a>Näide

Saate konfigureerida elektroonilise aruandluse (ER) vormingu looma väljamineva dokumendi Microsoft Office’i vormingus (Exceli töövihikud või Wordi dokumendid), kasutades eelmääratletud malli. See mall võib sisaldada QR-koodi pildi kohatäitena objekti **Pilt** (Exceli töövihik) või **Pildisisu juhtelement** (Wordi dokument). Peate lisama konfigureeritud ER-vormingule elemendi **Lahter**, mida kasutatakse selle kohatäite täitmiseks. Et määrata, millist teavet QR-koodis talletatakse, peate määrama sidumise sellele elemendile **Lahter**. Näiteks saate konfigureerida sellise sidumise, mis sisaldab järgmist avaldist:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Kui käitate konfigureeritud ER-vormingut, siis kasutatakse andmeallika **model.ListOfShelfLabels** välja **LabelText** teksti väärtust QR-koodi pildi loomiseks. See pilt asendab QR-koodi pildi kohatäite dokumendi mallis, mida kasutatakse väljamineva dokumendi loomiseks. Kui loodud dokumendi pilt on skannitud, tagastab see teksti, mis võeti mudeli andmeallika **model.ListOfShelfLabels** väljalt **LabelText**. Lisateavet vt teemast [Piltide ja vormide manustamine ER-i abil loodavatesse dokumentidesse](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
