---
title: ER-i funktsioon QRCODE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni QRCODE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 92665936decc87b29f2fabb346f4d16745d0a30b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562657"
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