---
title: ER-i funktsioon VALUEIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUEIN.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: e5a0ac314a61abce610407550e65479cbf5a6b5b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565828"
---
# <a name="valuein-er-function"></a>ER-i funktsioon VALUEIN

[!include [banner](../includes/banner.md)]

Funktsioon `VALUEIN` määratleb, kas määratud sisend vastab määratud loendis määratud üksuse mis tahes väärtusele. See tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul. Muidu tagastab see *kahendväärtuse* **VÄÄR**.

## <a name="syntax"></a>Süntaks

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumendid

`input`: *väli*

Tüübi *Kirjete loend* andmeallika üksuse kehtiv tee. Selle üksuse väärtus vastendatakse.

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`list item expression`: *kahendmuutuja*

Kehtiv tingimuslik avaldist, mis osutab või sisaldab määratletud loendi üksikut välja, mida tuleks kasutada vastendamiseks.

## <a name="return-values"></a>Tagastusväärtused

*Kahendmuutuja*

Tulemiks saadud *kahendmuutuja* väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Üldiselt on funktsioon `VALUEIN` tõlgitud kui tingimuste **OR** kogumit. Kui tingimuste **OR** loend on suur ja SQL-lause maksimaalne kogupikkus võidakse ületada, kaaluge funktsiooni [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) kasutamist.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

Mõnel juhul saab selle teisendada andmebaasi SQL-lauseks, kasutades `EXISTS JOIN` tehtemärki.

## <a name="example-1"></a>Näide 1

Mudeli vastendamises saate määratleda tüübi *Arvutatud väli* andmeallika **Loend**. See andmeallikas sisaldab avaldist `SPLIT ("a,b,c", ",")`.

Andmeallika kutsumisel, kui see on konfigureeritud avaldisena `VALUEIN ("B", List, List.Value)`, tagastab see väärtuse **TRUE**. Sellisel juhul on funktsioon `VALUEIN` tõlgitud järgmiseks tingimuste kogumiks: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, kus `("B" = "b")` on võrdne tulemusega **TRUE**.

Andmeallika kutsumisel, kui see on konfigureeritud avaldisena `VALUEIN ("B", List, LEFT(List.Value, 0))`, tagastab see väärtuse **FALSE**. Sellisel juhul on funktsioon `VALUEIN` tõlgitud järgmiseks tingimuseks: `("B" = "")`, mis ei ole võrdne tulemusega **TRUE**.

Taolise tingimuse teksti tähemärkide arvu ülempiir on 32 768 tähemärki. Seetõttu ei tohiks te luua andmeallikaid, mis võivad käitusajal seda piirangut ületada. Kui piirang ületatakse, lõpetab rakendus töötamise ja esitatakse erand. Selline olukord võib tekkida näiteks siis kui andmeallikas konfigureeritakse kui `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` ja loendid **Loend1** ning **Loend2** sisaldavad suurt hulka kirjeid.

Mõnel juhul tõlgitakse funktsioon `VALUEIN` andmebaasi aruandeks, kasutades `EXISTS JOIN` tehtemärki. See juhtub, kui kasutatakse funktsiooni [`FILTER`](er-functions-list-filter.md) ja järgmised tingimused on täidetud.

- Suvand **ASK FOR QUERY** on funktsiooni `VALUEIN` andmeallika jaoks välja lülitatud, mis viitab kirjete loendile. Sellele andmeallikale ei rakendada käitusajal lisatingimusi.
- Pesastatud avaldisi ei ole andmeallika funktsiooni `VALUEIN` jaoks konfigureeritud, mis viitab kirjete loendile.
- Funktsiooni `VALUEIN` loendi üksus viitab määratletud andmeallika väljale, mitte avaldisele ega meetodile.

Kaaluge selle suvandi kasutamist funktsiooni [`WHERE`](er-functions-list-where.md) asemel, nagu selles näites varasemalt kirjeldatud.

## <a name="example-2"></a>Näide 2

Määratlege oma mudelivastenduses järgmised andmeallikad.

- Tüübi *Tabeli kirjete* andmeallikas **Sisse**. See andmeallikas viitab intrastati tabelile.
- Tüübi *Tabeli kirjete* andmeallikas **Port**. See andmeallikas viitab tabelile IntrastatPort.

Kui kutsutakse andmeallikas, mis on konfigureeritud kui avaldis `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, luuakse intrastati tabeli filtreeritud kirjete tagastamiseks järgmine SQL-lause.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Väljade **dataAreaId** jaoks luuakse lõplik SQL-lause, kasutades tehtemärki `IN`.

## <a name="example-3"></a>Näide 3

Määratlege oma mudelivastenduses järgmised andmeallikad.

- Tüübi *Arvutatud väli* andmeallikas **Le**. See andmeallikas sisaldab avaldist `SPLIT ("DEMF,GBSI,USMF", ",")`.
- Tüübi *Tabeli kirjete* andmeallikas **Sisse**. See andmeallikas viitab intrastati tabelile ja suvand **Ettevõtteülene** on selle jaoks sisse lülitatud.

Kui kutsutakse andmeallikas, mis on konfigureeritud avaldisena `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, sisaldab lõplik SQL-i aruanne järgmist tingimust.

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)

[VALUEINLARGE funktsioonid](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]