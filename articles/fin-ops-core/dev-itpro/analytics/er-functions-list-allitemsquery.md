---
title: ER-i funktsioon ALLITEMSQUERY
description: See artikkel annab teavet selle kohta, kuidas kasutatakse funktsiooni ALLITEMSQUERY Electronic Reporting (ER).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f5f8c69e7f67377c2e3d9ccc5a0da1fefe488921
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877150"
---
# <a name="allitemsquery-er-function"></a>ER-i funktsioon ALLITEMSQUERY

[!include [banner](../includes/banner.md)]

Funktsioon `ALLITEMSQUERY` töötab liidetud SQL-päringuna. See tagastab uue tasandatud *kirjete loendi* väärtuse, mis koosneb kirjete, mis tähistavad kõiki määratud teele vastavaid üksuseid, loendist.

## <a name="syntax"></a>Süntaks

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Argumendid

`path`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee. See peab sisaldama vähemalt ühte seost.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Määratud tee peab olema määratletud andmetüübi *Kirjete loend* andmeallika elemendi kehtiva andmeallika teena. Lisaks peab see sisaldama vähemalt ühte seost. Andmeelemendid, nagu tee *string* või *kuupäev*, peaks elektroonilise aruandluse (ER) avaldisekoostajas andma koostamise ajal tõrke.

Kui seda funktsiooni rakendatakse andmetüübi *Kirjete loend* andmeallikatele, mis viitavad rakendusobjektile, mida saab SQL-i abil otse kutsuda (nt tabel, üksus või päring), töötab see ühendatud SQL-päringuna. Vastasel juhul töötab see mälus funktsioonina [ALLITEMS](er-functions-list-allitems.md).

## <a name="example"></a>Näide

Määratlege oma mudelivastenduses järgmised andmeallikad.

- Tüübi **Tabelikirjed** andmeallikas *CustInv*, mis viitab tabelile CustInvoiceTable
- Tüübi *Arvutatud väli* andmeallikas **FilteredInv**, mis sisaldab avaldist `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- Tüübi *Arvutatud väli* andmeallikas **JourLines**, mis sisaldab avaldist `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

Kui käitate mudelivastenduse andmeallika **JourLines** poole pöördumiseks, käivitatakse järgmine SQL-avaldis.

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]