---
title: ER-i funktsioon ORDERBY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ORDERBY.
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
ms.openlocfilehash: 963d55bcf98a9109c8b6ceb57edf5b55f15a2b0f
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075170"
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
> Seda süntaksit toetatakse Microsofti Dynamics 365 Finance versiooni 10.0.25 ja uuema versiooni puhul.

## <a name="arguments"></a>Argumendid

`location`: *[String](er-formula-supported-data-types-primitive.md#string)*

Asukoht, kus sortimist tuleks käitada. Kehtivad järgmised suvandid.

- "Päring"
- "InMemory"

`list`: *[Kirjeloend](er-formula-supported-data-types-composite.md#record-list)*

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

Andmete sorteerimine toimub alati rakenduse serveri mälus. Lisateavet leiate näitest [1](#example-1).

### <a name="syntax-2"></a>Süntaks 2

### <a name="sorting-in-memory"></a>Sortimine mälus

Kui argumendiks `location` on määratud **InMemory**, toimub andmete sortimine rakenduseserveri mällu. Lisateavet leiate näitest [2](#example-2).

### <a name="sorting-in-database"></a>Sortimine andmebaasis

`location` Kui argument on määratud **päringuna**, toimub andmete sortimine andmebaasi tasemel. Sellisel juhul peab argument osutama ühele järgmistest `list` elektroonilise aruandluse (ER) [andmeallikatest,](general-electronic-reporting.md) mis täpsustab rakenduse allika, mille jaoks saab luua otsese andmebaasipäringu:

- Tabelikirjete *tüübi andmeallikas*
- Tabelikirjete *tüübi* andmeallika seos
- Välja *Arvutustüübi andmeallikas*

Argumendid `expression 1` ja `expression N` argumendid peavad osutama ER-andmeallika väljadele, mis täpsustavad rakenduse allika asjakohased väljad, millele saab luua ka otsese andmebaasipäringu.

Kui otsest andmebaasipäringut ei saa luua, ilmneb ER-mudelivastenduse kujundajas [valideerimistõrge](er-components-inspections.md#i18). Teile kuvatavas teates on kirjas, et ER-i avaldist, mis sisaldav funktsiooni `ORDERBY` ei saa käitusajal käivitada.

Parema jõudluse tagamiseks soovitame kasutada **suvandit Päring**, kui sortimine on konfigureeritud rakenduse andmeallikate jaoks, mis võivad sisaldada suurt hulka kirjeid (nt tehingurakendustabelite puhul).

> [!NOTE]
> Funktsiooni `ORDEBY` ennast ei saa otseandmebaasi päringusse tõlkida. Seetõttu pole seda funktsiooni sisaldav ER-andmeallikas küsitav. Seda ei saa kasutada ka ER-funktsioonide (nt [FILTER](er-functions-list-filter.md) ja [ALLITEMSQUERY](er-functions-list-allitemsquery.md)) ulatuses, kus saab kasutada ainult päringuid kasutatavaid andmeallikaid.

Lisateavet leiate näitest [3](#example-3) ja [näitest 4](#example-4).

### <a name="comparability"></a>Võrreldavus

Kuna SQL-andmebaasimootor ja Finance'i rakendusserver saavad ühe märgi jaoks kasutada erinevat järjestusväärtust, võib sama kirjete loendi sortimistulemus erineda, kui [sortimiseks kasutatakse stringivälja](er-formula-supported-data-types-primitive.md#string). Lisateavet leiate näitest [5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a> Näide 1: mälus vaikekäivitus

Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("C|B|A", "|")`, tagastab avaldis `FIRST( ORDERBY( DS, DS. Value)).Value` teksti väärtuse **„A”**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a> Näide 2: mälus selgesõnaline täitmine

Kui **hankija** on konfigureeritud tabelikirjete *tüübi* ER andmeallikana, mis viitab tabelile **VendTable**, tagastavad nii avaldis `ORDERBY (Vendor, Vendor.'name()')` kui ka avaldis `ORDERBY ("InMemory", Vendor, Vendor.'name()')` hankijate loendi, mis on järjestatud nime järgi tõusvas järjestuses.

Avaldise `ORDERBY ("Query", Vendor, Vendor.'name()')` konfigureerimisel ER-mudelivastenduse kujundajas ilmneb valideerimisviga [kujundusajal](er-components-inspections.md#i8), kuna `Vendor.'name()'` tee viitab rakendusmeetodile, millel on loogika, mida ei saa otseandmebaasi päringusse tõlkida.

## <a name="example-3-database-query"></a><a name="example-3"></a> Näide 3: andmebaasi päring

Kui **TaxTransaction** on konfigureeritud tabelikirjete *tüübi* ER andmeallikana, mis viitab tabelile **TaxTrans**, sordib avaldis `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` kirjed rakenduse andmebaasi tasemel ja tagastab maksukannete loendi, mis on järjestatud maksukoodi järgi tõusvas järjestuses.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a> Näide 4: küsitavad andmeallikad

Kui **TaxTransaction** on konfigureeritud tabelikirjete *tüübi* ER andmeallikana, mis viitab tabelile **TaxTrans**, **saab taxTransactionFiltered** ER andmeallika konfigureerida nii, et see sisaldab avaldist`FILTER(TaxTransaction, TaxCode="VAT19")`, mis toob kannete määratud maksukoodi jaoks. Kuna konfigureeritud **TaxTransactionFiltered** ER andmeallikas on päringuga, avaldis`ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` saab konfigureerida tagastama filtreeritud maksutehingute loendi, mis on sorteeritud tehingukuupäeva järgi kasvavas järjekorras.

Kui konfigureerite **TaxTransactionOrdered** ER andmeallikana *Arvutatud väli* tüüp, mis sisaldab väljendit`ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` ja ER andmeallikas *Arvutatud väli* tüüp, mis sisaldab väljendit`FILTER(TaxTransactionOrdered, TaxCode="VAT19")`, kinnitus [viga](er-components-inspections.md#i18) toimub projekteerimise ajal ER mudeli kaardistamise kujundajas. See viga ilmneb, kuna esimene argument [FILTER](er-functions-list-filter.md#usage-notes) funktsioon peab viitama päringutavale ER-i andmeallikale, kuid **TaxTransactionOrdered** andmeallikas, mis sisaldab`ORDERBY` funktsioon ei ole küsitav.

## <a name="example-5-comparability"></a><a name="example-5"></a> Näide 5: Võrreldavus

### <a name="prerequisites"></a>Eeltingimused

1. Sisestage andmeallikas **DS1** selle *Arvutatud väli* tüüp, mis sisaldab väljendit `SPLIT ("D1|_D2|D3", "|")`.
2. Ava **[Finantsdimensiooni väärtused](../../../finance/general-ledger/financial-dimensions.md)** leht ja valige **Kulukeskus** dimensioon.
3. Sisestage järgmised dimensioonide väärtused: **D1**,**\_ D2**, ja **D3**.

### <a name="sorting-in-memory"></a>Sortimine mälus

1. Andmeallika konfigureerimine **DS2** selle *Arvutatud väli* tüüp, mis sisaldab väljendit `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Pange tähele, et väljend`FIRST(DS2).Value` tagastab teksti väärtuse **"D1"**, väljend`INDEX(DS2, COUNT(DS2)).Value` tagastab teksti väärtuse **"\_ D2"**, ja väljend`STRINGJOIN(DS2, DS2.Value, "|")` tagastab teksti väärtuse **"D1\| D3\|\_ D2"**.

### <a name="sorting-in-database"></a>Sortimine andmebaasis

1. Sisestage andmeallikas **DS3** selle *Tabelikirjed* tüüp, mis viitab **FinancialDimensionValueEntity** üksus.
2. Andmeallika konfigureerimine **DS4** selle *Arvutatud väli* tüüp, mis sisaldab väljendit `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Andmeallika konfigureerimine **DS5** selle *Arvutatud väli* tüüp, mis sisaldab väljendit `ORDERBY(DS4, DS4.DimensionValue)`.
4. Pange tähele, et väljend`FIRST(DS5).Value` tagastab teksti väärtuse **"\_ D2"**, väljend`INDEX(DS5, COUNT(DS5)).Value` tagastab teksti väärtuse **"D3"**, ja väljend`STRINGJOIN(DS5, DS5.Value, "|")` tagastab teksti väärtuse **"\_ D2\| D1\| D3"**.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
