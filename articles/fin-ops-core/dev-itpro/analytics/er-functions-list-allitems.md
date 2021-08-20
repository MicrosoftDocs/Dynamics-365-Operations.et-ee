---
title: ER-i funktsioon ALLITEMS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ALLITEMS.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cf1e05e9377ba18ad0269a48b13bd242a8e5356f4a52ea3723e347dcf5e138e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719844"
---
# <a name="allitems-er-function"></a>ER-i funktsioon ALLITEMS

[!include [banner](../includes/banner.md)]

Funktsioon `ALLITEMS` töötab mälusisese valikuna ja tagastab uue tasandatud *kirjete loendi* väärtuse kirjete loendina, mis tähistab kõiki määratud teele vastavaid üksuseid.

## <a name="syntax"></a>Süntaks

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumendid

`path`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Tee peab olema määratletud andmetüübi *Kirjete loend* andmeallika elemendi kehtiva andmeallika teena. Andmeelemendid, nagu tee string või kuupäev, peaks elektroonilise aruandluse (ER) avaldisekoostajas andma koostamise ajal tõrke.

Seda funktsiooni ei ole soovitatav kandeandmete allikate puhul, mis võivad sisaldada suurt hulka andmeid. Selle asemel kaaluge funktsiooni [ALLTEMSQUERY](er-functions-list-allitemsquery.md) kasutamist.

## <a name="example-1"></a>Näide 1

Kui sisestate olemi `SPLIT("abcdef" , 2)` andmeallikana **DS**, tagastab avaldis `COUNT( ALLITEMS (DS))` tulemuse **3**.

## <a name="example-2"></a>Näide 2

Kui sisestate suvandi **Hankija** andmetüübi *Kirjete loend* andmeallikana, mis viitab rakendustabelile VendTable, tagastab avaldis `ALLITEMS (Vend.'<Relations'.ContactPerson)` tasandatud kirjete loendi, millel on tabeli struktuur **ContactPerson** ja sisaldab kõiki kontaktisikuid, kellele on võimalik pääseda juurde seost **ContactPerson.ContactForParty == VendTable.Party** kasutades, ning mis on saadaval kõikidele viidatud hankijatabeli hankijatele.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]