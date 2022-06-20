---
title: ER-i funktsioon FILTER
description: See artikkel annab teavet selle kohta, kuidas filtreerida elektroonilise aruandluse (ER) funktsiooni.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: dfa4afdcfad8c1855a10e1fa37c36cc5b20682ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884513"
---
# <a name="filter-er-function"></a>ER-i funktsioon FILTER

[!include [banner](../includes/banner.md)]

Funktsioon `FILTER` tagastab määratud loendi *kirjete loendi* väärtusena pärast seda, kui päringut on muudetud nii, et see filtreerib määratud tingimuse jaoks.

## <a name="syntax"></a>Süntaks

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`condition`: *kahendmuutuja*

Kehtiv tingimuslik avaldis, mida kasutatakse määratud loendi kirjete filtreerimiseks.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a><a name="usage-notes"></a>Kasutamise märkused

Erinevalt funktsioonist [WHERE](er-functions-list-where.md) rakendatakse määratud tingimust andmebaasi tasemel kõigile tüübi *Tabeli kirjed* elektroonilise aruandluse (ER) andmeallikatele. Loendi ja tingimuse saab määrata tabelite ja seoste abil.

Kui üks või mõlemad argumendid, mis on selle funktsiooni jaoks konfigureeritud (`list` ja `condition`), ei luba seda taotlust otsesesse SQL-kutsesse tõlkida, esitatakse kujundamise ajal erand. See erand teavitab kasutajat, et funktsiooni `list` või `condition` ei saa andmebaasi päringuks kasutada.

> [!NOTE]
> Funktsioon `FILTER` erineb funktsioonist `WHERE`, kui funktsiooni [`VALUEIN`](er-functions-logical-valuein.md) kasutatakse valikukriteeriumide määramiseks.
> 
> - Kui funktsiooni `VALUEIN` kasutatakse funktsiooni `WHERE` ulatuses ja teine argument viitab andmeallikale, `VALUEIN` mis ei tagasta ühtegi kirjet, viidatakse Kahendmuutuja väärale *[...](er-formula-supported-data-types-primitive.md#boolean)*`VALUEIN` väärtusele, mis tagastab. Seega ei tagasta avaldis `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` hankija kirjeid, kui **VendGroupsi andmeallikas** ei tagasta hankijagrupi kirjeid.
> - Kui funktsiooni `VALUEIN` kasutatakse funktsiooni ulatuses ja teine argument viitab andmeallikale, `FILTER` mis ei tagasta ühtegi kirjet, ignoreeritakse Kahendmuutuja `VALUEIN`*[...](er-formula-supported-data-types-primitive.md#boolean)* väära väärtust, mis tagastab.`VALUEIN` Seega avaldis tagastab `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` hankijate andmeallika **kõik hankijakirjed** ka siis, **kui andmeallikas VendGroups** ei tagasta hankijagrupi kirjeid.

## <a name="example-1"></a>Näide 1

Kui **Hankija** on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `FILTER (Vendors, Vendors.VendGroup = "40")` loendi ainult hankijatega, mis kuuluvad hankijate gruppi 40.

## <a name="example-2"></a>Näide 2

Kui **Hankija** on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, ja kui **parmVendorBankGroup** on konfigureeritud ER-i andmeallikana, mis tagastab väärtuse andmetüübiga *String*, tagastab avaldis `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` loendi ainult nende hankijakontodega, mis kuuluvad kindlasse pangarühma.

## <a name="example-3"></a>Näide 3

Sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A,B,C", ",")`. Seejärel sisestage teine avaldis `FILTER( DS, DS.Value = "B")`. Kui proovite salvestada selle avaldise ER-i valemikoostajas, esitatakse järgmine erand: „Valideerimise viga: funktsiooni FILTER avaldiste loend ei saa olla päringuobjekt”.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
