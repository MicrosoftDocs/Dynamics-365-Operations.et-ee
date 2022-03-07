---
title: ER-i funktsioon VALUEINLARGE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUEINLARGE.
author: NickSelin
ms.date: 08/17/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 57b2246631b31cce10d086da29e76b729059a64aa6a3c2d8cf864dd70085dbfd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725256"
---
# <a name="valueinlarge-er-function"></a>ER-i funktsioon VALUEINLARGE

[!include [banner](../includes/banner.md)]

Funktsioon `VALUEINLARGE` määratleb, kas määratud *Int64* või *Täisarv*-tüüpi sisend vastab määratud loendis määratud üksuse mis tahes väärtusele. Funktsioon tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul. Muidu tagastab see *kahendväärtuse* **VÄÄR**. Erinevusest funktsiooniga `VALUEIN` aru saamiseks lugege selle teema hilisemat jaotist [Kasutusmärkus](#usage_note).

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