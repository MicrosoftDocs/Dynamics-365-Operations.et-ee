---
title: ER-i funktsioon ORDERBY
description: See artikkel annab teavet selle kohta, kuidas KASUTATAKSE ORDERBY elektroonilise aruandluse (ER) funktsiooni.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 23ace859bf75b2adb6ef8604475519a015486948
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282557"
---
# <a name="orderby-er-function"></a>ER-i funktsioon ORDERBY

[!include [banner](../includes/banner.md)]

Funktsioon `ORDERBY` tagastab määratud loendi *kirjete loendi* väärtusena, kui see on vastavalt määratud argumentidele sorditud. Neid argumente saab määratleda avaldistena.

## <a name="syntax-1"></a><a name="syntax-1"></a>Süntaks 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Süntaks 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Seda süntaksit toetab Microsoft Dynamics 365 finantsversioon 10.0.25 ja uuem versioon.

## <a name="arguments"></a>Argumendid

`location`: *[string](er-formula-supported-data-types-primitive.md#string)*

Asukoht, kus sortimist tuleks käitada. Kehtivad järgmised valikud:

- Päring
- InMemory

`list`: *[kirjeloend](er-formula-supported-data-types-composite.md#record-list)*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`expression 1`: *väli*

Andmeallika välja kehtiv tee, millele viitab kutsutud funktsiooni argument `list`. Viidatud väli peab olema primitiivse andmetüübi väli. See argument on kohustuslik.

`expression N`: *väli*

Andmeallika välja kehtiv tee, millele viitab kutsutud funktsiooni argument `list`. Viidatud väli peab olema primitiivse andmetüübi väli. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

### <a name="syntax-1"></a>Süntaks 1

Andmeid sorditakse alati rakendusserveri mälus. Lisateavet vt näitest [1](#example-1).

### <a name="syntax-2"></a>Süntaks 2

### <a name="sorting-in-memory"></a>Mälus sortimine

Kui argument `location` on määratud kui **InMemory**, toimub andmete sortimine rakendusserveri mälus. Lisateavet vt näitest [2](#example-2).

### <a name="sorting-in-database"></a>Sortimine andmebaasis

Kui argument `location` on määratud **päringuna**, toimub andmete sortimine andmebaasi tasemel. Sellisel juhul peab argument osutama ühele järgmistest elektroonilise aruandluse (ER)`list` andmeallikatest, mis määrab rakenduse allika, [mille](general-electronic-reporting.md) jaoks on võimalik luua otseandmebaasi päring:

- Tabelikirjete *tüübi andmeallikas*
- Tabelikirjete tüübi andmeallika *seos*
- Kalkulatsioonivälja *tüübi andmeallikas*

Need `expression 1` ja `expression N` argumendid peavad osutama ER-i andmeallika väljadele, mis määratlevad rakenduse allika asjakohased väljad, mille kohta saab teha ka otseandmebaasi päringu.

Kui otsese andmebaasi päringut ei saa luua, ilmneb kinnitamistõrge [ER](er-components-inspections.md#i18)-mudeli vastendamise kujundajas. Teile kuvatavas teates on kirjas, et ER-i avaldist, mis sisaldav funktsiooni `ORDERBY` ei saa käitusajal käivitada.

Paremaks jõudluseks soovitame kasutada valikut Päring, kui sortimine on konfigureeritud rakenduse andmeallikatele, **mis** võivad sisaldada suurt hulka kirjeid (nt kande rakenduse tabelite puhul).

> [!NOTE]
> Funktsiooni `ORDEBY` ennast ei saa otseandmebaasi päringuks tõlkida. Seetõttu ei saa seda funktsiooni sisaldava ER-i andmeallikas teha päringuid. Samuti ei saa seda kasutada selliste ER-funktsioonide [ulatuses nagu FILTER](er-functions-list-filter.md)[ja ALLITEMSQUERY](er-functions-list-allitemsquery.md), kus saab kasutada ainult päringusse kuuluvaid andmeallikaid.

Lisateavet vt näitest [3](#example-3) ja [näitest 4](#example-4).

### <a name="comparability"></a>Võrreldavus

Kuna SQL-andmebaasi mootor ja finantside rakendusserver saavad üksiku märgi jaoks kasutada erinevat reitinguväärtust, [võib sama kirjeloendi sortimistulemus stringivälja](er-formula-supported-data-types-primitive.md#string) sortimisel erineda. Lisateavet vt näitest [5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a> Näide 1: mälu vaikekäivitamine

Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("C|B|A", "|")`, tagastab avaldis `FIRST( ORDERBY( DS, DS. Value)).Value` teksti väärtuse **„A”**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a> Näide 2: mälus selgesõnaline käivitamine

Kui **hankija** on konfigureeritud VendTable-tabelile *viitavate tabelikirjete tüübi ER-andmeallikana* **·**, `ORDERBY (Vendor, Vendor.'name()')``ORDERBY ("InMemory", Vendor, Vendor.'name()')` siis on nii avaldis kui ka avaldis tagastanud kasvavas järjestuses nime alusel sorditud hankijate loendi.

Kui konfigureerite avaldise `ORDERBY ("Query", Vendor, Vendor.'name()')` ER-mudeli vastendamise kujundajas, [ilmneb](er-components-inspections.md#i8) kinnitamise tõrge kujunduse ajal, sest tee viitab rakendusmeetodile, `Vendor.'name()'` mille loogikat ei saa otseandmebaasi päringusse tõlkida.

## <a name="example-3-database-query"></a><a name="example-3"></a> Näide 3: andmebaasi päring

Kui **TaxTransaction** on konfigureeritud Tabelikirjete tüübi ER *andmeallikana*, mis viitab tabelile TaxTrans **, sordib avaldis kirjed rakenduse andmebaasi tasemel ja tagastab maksukannete loendi,** mis on sorditud maksukoodi järgi kasvavas `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` järjestuses.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a> Näide 4: päringute andmeallikad

**Kui TaxTransaction** on konfigureeritud *Tabelikirjete tüübi ER* **andmeallikana**, mis viitab tabelile TaxTrans **, saab TaxTransactionFiltered** ER-i andmeallika konfigureerida nii, et see sisaldab avaldist, `FILTER(TaxTransaction, TaxCode="VAT19")` mis toob kanded määratud maksukoodi jaoks. Kuna konfigureeritud **TaxTransactionFiltered** ER-i andmeallikas on päringutav, `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` saab avaldist konfigureerida, et tagastada filtreeritud maksukannete loend, mis on sorditud kande kuupäeva alusel kasvavas järjestuses.

Kui konfigureerite **TaxTransactionOrderedi** arvutatud väljatüübi *ER*`ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` andmeallikana, mis sisaldab avaldist ja avaldist sisaldava arvutatud väljatüübi *ER*`FILTER(TaxTransactionOrdered, TaxCode="VAT19")` andmeallikat, [ilmneb](er-components-inspections.md#i18) ER-mudeli vastendamise kujundajas kinnitamise tõrge. See tõrge ilmneb, sest FILTER-funktsiooni [esimene argument peab viitama päringule ER andmeallikale,](er-functions-list-filter.md#usage-notes) kuid funktsiooni sisaldav TaxTransactionOrdered **andmeallikas** `ORDERBY` pole päringut võimalik teha.

## <a name="example-5-comparability"></a><a name="example-5"></a> Näide 5: võrdlus

### <a name="prerequisites"></a>Eeltingimused

1. Sisestage avaldist sisaldava arvutatud **välja tüübi andmeallika** *DS1*.`SPLIT ("D1|_D2|D3", "|")`
2. Avage leht **[Finantsdimensiooni väärtused](../../../finance/general-ledger/financial-dimensions.md)** ja valige **CostCenteri** dimensioon.
3. Sisestage järgmised dimensiooniväärtused: **D1**, **\_ D2** ja **D3**.

### <a name="sorting-in-memory"></a>Mälus sortimine

1. Saate konfigureerida avaldist sisaldava arvutatud **väljatüübi** *andmeallika DS2*.`ORDERBY("InMemory", DS1, DS1.Value)`
2. Pange tähele `FIRST(DS2).Value`**, et avaldis tagastab tekstiväärtuse D1**, `INDEX(DS2, COUNT(DS2)).Value`**avaldis tagastab tekstiväärtuse "\_ D2"**`STRINGJOIN(DS2, DS2.Value, "|")`**ja avaldis tagastab teksti väärtuse "D1\| D3\|\_ D2"**.

### <a name="sorting-in-database"></a>Sortimine andmebaasis

1. Sisestage tabelikirjete **tüübi andmeallika DS3** *·*, mis viitab üksusele **FinancialDimensionValueEntity.**
2. Saate konfigureerida avaldist sisaldava arvutatud **väljatüübi** *andmeallika DS4*.`FILTER(DS3, DS3.FinancialDimension="CostCenter")`
3. Saate konfigureerida **avaldist sisaldava arvutatud** väljatüübi *andmeallika* DS5`ORDERBY(DS4, DS4.DimensionValue)`.
4. Pange tähele `FIRST(DS5).Value`**\_, et avaldis tagastab tekstiväärtuse D2**, `INDEX(DS5, COUNT(DS5)).Value`**avaldis tagastab tekstiväärtuse "D3"**`STRINGJOIN(DS5, DS5.Value, "|")`**ja avaldis tagastab teksti väärtuse "\_ D2\| D1\| D3".**

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
