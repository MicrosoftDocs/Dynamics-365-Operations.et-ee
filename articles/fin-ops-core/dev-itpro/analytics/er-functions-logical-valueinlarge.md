---
title: ER-i funktsioon VALUEINLARGE
description: See artikkel annab teavet selle kohta, kuidas valueINLARGE elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 08/17/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 425dbce8f229acbb9c8d721c8f1a554989e0533c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288074"
---
# <a name="valueinlarge-er-function"></a>ER-i funktsioon VALUEINLARGE

[!include [banner](../includes/banner.md)]

Funktsioon `VALUEINLARGE` määratleb, kas määratud *Int64* või *Täisarv*-tüüpi sisend vastab määratud loendis määratud üksuse mis tahes väärtusele. Funktsioon tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul. Muidu tagastab see *kahendväärtuse* **VÄÄR**. Funktsiooni erinevusest aru saada `VALUEIN` vt selle artikli [jaotisest](#usage_note) Kasutusmarve.

## <a name="syntax"></a>Süntaks

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumendid

`input`: *väli*

Tüübi *Kirjete loend* andmeallika üksuse kehtiv tee. Selle üksuse väärtus vastendatakse.

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`list item expression`: *Avaldis*

Kehtiv tingimuslik avaldist, mis osutab või sisaldab määratletud loendi üksikut välja, mida tuleks kasutada vastendamiseks.

## <a name="return-values"></a>Tagastusväärtused

*Kahendmuutuja*

Tulemiks saadud *kahendmuutuja* väärtus.

## <a name=""></a><a name="usage_note">Kasutamise märkused</a>

Kui määratud sisend tähistab *Int64* või *Täisarv* andmeallika tüüpi, mille kutse saab teisendada otseseks SQL-lauseks, teisendatakse määratud loend ajutiseks SQL-tabeliks ja vastendamine tehakse andmebaasis üksiku päringuga `EXISTS JOIN`. Muul juhul toimib funktsioon nagu funktsioon [`VALUEIN`](er-functions-logical-valuein.md).

Kui määratud sisend tähistab andmeallika üksust, mis on ette nähtud muu kui *Int64* ja *Täisarv*-tüüpi üksusena, ilmneb kujundusajal tõrge, mis teatab, et funktsiooni `VALUEINLARGE` ei saa konfigureeritud ER-lause jaoks rakendada.

Kui täidetakse funktsiooni `VALUEINLARGE` avaldist ja selle täitmises ulatuses kasutatakse rohkem kui ühte ajutist tabelit, ilmneb käitusaja tõrge.

## <a name="example"></a>Näide

Määratlege oma mudelivastenduses järgmised andmeallikad.

- Tüübi *Tabeli kirjete* andmeallikas **Sisse**.
    - See andmeallikas viitab tabelile **Intrastat**.
    - Suvand **Kontsernisisene** seatakse väärtusele **Ei**.
- Tüübi *Arvutatud väli* andmeallikas **InMemory**.
    - See andmeallikas sisaldab avaldist `WHERE (In, In.Port <> "")`.
- Tüübi *Arvutatud väli* andmeallikas **InFiltered**.
    - See andmeallikas sisaldab avaldist `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Kui andmeallikas **InFiltered** kutsutakse ettevõtte **DEMF** kontekstis, luuakse rakenduse andmebaasis uus, ajutine tabel. Sellesse tabelisse lisatakse kirje ID-de mällu kogutud loend ja tabeli **Intrastat** filtreeritud kirjete tagastamiseks genereeritakse järgmine SQL-lause.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Lisaressursid

[Loogilised funktsioonid](er-functions-category-logical.md)

[VALUEIN funktsioonid](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
