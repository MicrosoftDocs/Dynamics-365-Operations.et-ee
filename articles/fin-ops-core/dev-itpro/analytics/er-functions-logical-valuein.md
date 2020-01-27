---
title: ER-i funktsioon VALUEIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUEIN.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915966"
---
# <a name="VALUEIN">ER-i funktsioon VALUEIN</a>

[!include [banner](../includes/banner.md)]

Funktsioon `VALUEIN` määratleb, kas määratud sisend vastab määratud loendis määratud üksuse mis tahes väärtusele. See tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul. Muidu tagastab see *kahendväärtuse* **VÄÄR**.

## <a name="syntax"></a>Süntaks

```
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

Üldiselt on funktsioon `VALUEIN` tõlgitud kui tingimuste **OR** kogumit.

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

Mõnel juhul saab selle teisendada andmebaasi SQL-lauseks, kasutades `EXISTS JOIN` tehtemärki.

## <a name="example-1"></a>Näide 1

Mudeli vastendamises saate määratleda tüübi *Arvutatud väli* andmeallika **Loend**. See andmeallikas sisaldab avaldist `SPLIT ("a,b,c", ",")`.

Andmeallika kutsumisel, kui see on konfigureeritud avaldisena `VALUEIN ("B", List, List.Value)`, tagastab see väärtuse **TRUE**. Sellisel juhul on funktsioon `VALUEIN` tõlgitud järgmiseks tingimuste kogumiks: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, kus `("B" = "b")` on võrdne tulemusega **TRUE**.

Andmeallika kutsumisel, kui see on konfigureeritud avaldisena `VALUEIN ("B", List, LEFT(List.Value, 0))`, tagastab see väärtuse **FALSE**. Sellisel juhul on funktsioon `VALUEIN` tõlgitud järgmiseks tingimuseks: `("B" = "")`, mis ei ole võrdne tulemusega **TRUE**.

Taolise tingimuse teksti tähemärkide arvu ülempiir on 32 768 tähemärki. Seetõttu ei tohiks te luua andmeallikaid, mis võivad käitusajal seda piirangut ületada. Kui piirang ületatakse, lõpetab rakendus töötamise ja esitatakse erand. Selline olukord võib tekkida näiteks siis kui andmeallikas konfigureeritakse kui `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` ja loendid **Loend1** ning **Loend2** sisaldavad suurt hulka kirjeid.

Mõnel juhul tõlgitakse funktsioon `VALUEIN` andmebaasi aruandeks, kasutades `EXISTS JOIN` tehtemärki. See juhtub, kui kasutatakse funktsiooni [FILTER](er-functions-list-filter.md) ja järgmised tingimused on täidetud.

- Suvand **ASK FOR QUERY** on funktsiooni `VALUEIN` andmeallika jaoks välja lülitatud, mis viitab kirjete loendile. Sellele andmeallikale ei rakendada käitusajal lisatingimusi.
- Pesastatud avaldisi ei ole andmeallika funktsiooni `VALUEIN` jaoks konfigureeritud, mis viitab kirjete loendile.
- Funktsiooni `VALUEIN` loendi üksus viitab määratletud andmeallika väljale, mitte avaldisele ega meetodile.

Kaaluge selle suvandi kasutamist funktsiooni [WHERE](er-functions-list-where.md) asemel, nagu selles näites varasemalt kirjeldatud.

## <a name="example-2"></a>Näide 2

Määratlege oma mudelivastenduses järgmised andmeallikad.

- Tüübi *Tabeli kirjete* andmeallikas **Sisse**. See andmeallikas viitab intrastati tabelile.
- Tüübi *Tabeli kirjete* andmeallikas **Port**. See andmeallikas viitab tabelile IntrastatPort.

Kui kutsutakse andmeallikas, mis on konfigureeritud kui avaldis `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, luuakse intrastati tabeli filtreeritud kirjete tagastamiseks järgmine SQL-lause.

```
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

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)
