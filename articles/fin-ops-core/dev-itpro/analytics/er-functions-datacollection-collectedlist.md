---
title: ER-i funktsioon COLLECTEDLIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni COLLECTEDLIST.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d02f9ac4697a4d65417e522bffb5f40ebfdc237a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681228"
---
# <a name="collectedlist-er-function"></a>ER-i funktsioon COLLECTEDLIST

[!include [banner](../includes/banner.md)]

Funktsioon `COLLECTEDLIST` on *kirjete loendi* väärtus, mis sisaldab nende väärtuste loendit, mis on tagastatud vorminguelementide atribuudi **Kogutud andmete võtme väärtus** poolt ja kogutud, kui vorminguelemente kasutati väljaminevate dokumentide loomisel vormingu käitamise ajal, ja mis vastab määratud tingimustele. Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest.

## <a name="syntax"></a>Süntaks

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Argumendid

`condition 1 range`: *string*

Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud elektroonilise aruandluse (ER) vormingu komponendi atribuudis **Kogutud andmete võtme nimi**. See argument on kohustuslik.

`condition 1 value`: *string*

Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme väärtus**. See argument on kohustuslik.

`condition N range`: *string*

Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme nimi**. Need täiendavad argumendid on valikulised.

`condition N value`: *string*

Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme väärtus**. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Atribuute **Kogutud andmete võtme nimi** ja **Kogutud andmete võtme väärtus** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.

See funktsioon tagastab tühja loendi, kui praeguse komponendi **Üldine\\Fail** suvand **Kogu väljundi üksikasjad** on välja lülitatud.

Argumentides `condition range` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.

Argumentides `condition value` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.

## <a name="example"></a>Näide

Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest [ER-i loendamise ja liitmise vormingu väljundi kasutusandmed](tasks/er-format-counting-summing-1.md), mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa.

## <a name="additional-resources"></a>Lisaressursid

[Andmete kogumise funktsioonid](er-functions-category-data-collection.md)
