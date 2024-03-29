---
title: Elektroonilise aruandluse valemi keel
description: See artikkel annab teavet selle kohta, kuidas kasutada valemikeelt elektroonilises aruandluses (ER).
author: kfend
ms.date: 05/04/2020
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7df29c74b2a430ed9d974cad709b975e4fd9cd35
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283279"
---
# <a name="electronic-reporting-formula-language"></a>Elektroonilise aruandluse valemi keel

[!include [banner](../includes/banner.md)]

Elektrooniline aruandlus (ER) pakub võimsat andmete teisenduse kogemust. [ER-i valemikoostajas](general-electronic-reporting-formula-designer.md) nõutavate andmemanipulatsioonide väljendamiseks kasutatav keel meenutab valemi keelt Microsoft Excelis.

## <a name="basic-syntax"></a>Põhisüntaks

ER-i avaldised võivad sisaldada mõnd või kõiki järgmistest elementidest.

- [Konstandid](#Constants)
- [Tehtemärgid](#Operators)
- [Viited](#References)
- [Teed](#Paths)
- [Funktsioonid](#Functions)

## <a name="constants"></a><a name="Constants"></a>Konstandid

Avaldiste koostamisel saate kasutada tekstilisi ja arvulisi konstante (st väärtused, mida ei arvutata). Näiteks avaldis `VALUE ("100") + 20` kasutab arvulist konstanti **20** ja stringi konstanti **100** ning see tagastab arvulise väärtuse **120**.

ER-i valemikoostaja toetab paoseeriaid. Seega saate määrata avaldise stringi, mida tuleb teisiti käsitleda. Näiteks tagastab avaldis `"Leo Tolstoy ""War and Peace"" Volume 1"` tekstistringi **Lev Tolstoi „Sõda ja rahu” 1. osa**.

## <a name="operators"></a><a name="Operators"></a>Operaatorid

Järgmises tabelis on aritmeetilised tehtemärgid, mida saate kasutada põhiliste matemaatiliste tehete puhul, nagu liitmine, lahutamine, korrutamine ja jagamine.

| Operaator | Tähendus               | Näide     |
|----------|-----------------------|-------------|
| +        | Lisa              | `1+2`       |
| -        | Lahutamine, negatiivsus | `5-2`, `-1` |
| \*       | Korrutamine        | `7\*8`      |
| /        | Jaotus              | `9/3`       |

Järgmises tabelis kuvatakse toetatud võrdlemise tehtemärgid. Neid tehtemärke saate kasutada kahe väärtuse võrdlemiseks.

| Operaator | Tähendus                  | Näide      |
|----------|--------------------------|--------------|
| =        | Võrdne                    | `X=Y`        |
| &gt;     | Suurem kui             | `X>Y`        |
| &lt;     | Väiksem kui                | `X<Y`        |
| &gt;=    | Suurem kui või võrdne | `X>=Y`       |
| &lt;=    | Väiksem kui või võrdne    | `X<=Y`       |
| &lt;&gt; | Pole võrdne             | `X<>Y`       |

Peale selle saate kasutada ja-märki (&) teksti liitmise tehtemärgina. Nii saate ühe või mitu tekstistringi üheks tekstiks ühendada või liita.

| Operaator | Tähendus     | Näide                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Ühenda | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Tehete järjestus

Liitavaldise osade arvutamise järjekord on oluline. Näiteks avaldise `1 + 4 / 2` tulemid erinevad olenevalt sellest, kas esimesena tehakse liitmis- või jagamistoiming. Saate kasutada sulge, et selgelt määratleda, kuidas avaldise väärtust leida. Näiteks näitamaks, et esimesena tuleb teha liitmistoiming, saate muuta eelnevat avaldis järgmiselt: `(1 + 4) / 2`. Kui avaldise tehete järjekord ei ole selgelt määratletud, põhineb see vaikejärjestusel, mis on määratud toetatud tehtemärkidele. Järgmises tabelis on toodud igale tehtemärgile määratud järjestus. Kõrgema prioriteediga tehted (nt 7) arvutatakse enne madalama prioriteediga tehteid (nt 1).

| Tehtejärjestus | Tehtemärgid      | Süntaks                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Grupeerimine       | ( … )                                                                   |
| 6          | Liikme juurdepääs  | … . …                                                                   |
| 5          | Funktsioonikutse  | … ( … )                                                                 |
| 4          | Korrutamine | … \* …<br>… / …                                                         |
| 3          | Täiend       | … + …<br>… - …                                                          |
| 2          | Võrdlus     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Lahutamine     | … , …                                                                   |

Kui avaldis sisaldab mitut järjestikust sama järjestusega tehet, tehakse neid tehteid vasakult paremale. Näiteks avaldis `1 + 6 / 2 \* 3 > 5` tagastab väärtuse **tõene**. Soovitame avaldise tehete soovitud järjestuse selgeks näitamiseks kasutada sulge, et avaldisi oleks lihtsam lugeda ja hallata.

## <a name="references"></a><a name="References"></a>Viited

Kõiki praeguse ER-i komponendi andmeallikaid, mis on avalduse koostamise ajal saadaval, saab kasutada nimega viidetena. Praegune ER-i komponent saab olla kas mudel või vorming. Näiteks praegune ER-i mudelivastendus sisaldab **ReportingDate** andmeallikat, mis tagastab andmetüübi [*DateTime*](er-formula-supported-data-types-primitive.md#datetime) väärtuse. Loodavas dokumendis väärtuse õigesti vormindamiseks saate viidata avaldises andmeallikale järgmiselt: `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Kõikidele viidatava andmeallika nimes olevatele tähemärkidele, mis ei kuulu tähestikku, peab eelnema ühekordne jutumärk ('). Kui viidatava andmeallika nimi sisaldab vähemalt ühte sümbolit, mis ei kuulu tähestikku, tuleb nimi panna ühekordsetesse jutumärkidesse. Näiteks võivad need tähestikku mittekuuluvad sümbolid olla kirjavahemärgid või mis tahes muud kirjalikud sümbolid. Järgmisena on toodud mõned näited.

- Andmeallikale **Tänane kuupäev ja kellaaeg** tuleb viidata ER-i avaldises järgmiselt: `'Today''s date & time'`.
- ER-i avaldises tuleb viidata andmeallika **Kliendid** meetodile **nimi()** järgmiselt: `Customers.'name()'`.

Kui rakenduse andmeallikate meetoditel on parameetrid, kasutatakse järgmist süntaksit.

- Kui **onKeelRTL** andmeallika **Süsteem** meetod andmetüübil on **EN-US** parameeter [*string*](er-formula-supported-data-types-primitive.md#string) andmetüübil, peab see meetod olema ER-avaldises viidatud järgmisel viisil `System.isLanguageRTL("EN-US")`.
- Kui meetodi nimi sisaldab ainult tähti ja numbreid, siis ei ole jutumärgid vajalikud. Need on aga vajalikud sulgusid sisaldava tabelimeetodi puhul.

Kui andmeallikas **Süsteem** lisatakse ER-vastendusele, mis viitab rakendusklassile **Üldine**, siis annab avaldis `System.isLanguageRTL("EN-US ")` *kahendmuutuja* väärtuse **FALSE**. Muudetud avaldis `System.isLanguageRTL("AR")` annab vastuseks *kahendmuutuja* väärtuse **TRUE**.

Saate piirata, kuidas väärtusi selle meetoditüübi parameetritele edastatakse.

- Seda tüüpi meetoditele saab edastada ainult konstante. Konstantide väärtused määratakse koostamisajal.
- Seda tüüpi parameetrite puhul toetatakse ainult [primitiivseid](er-formula-supported-data-types-primitive.md) (põhilisi) andmetüüpe. Primitiivsed andmetüübid hõlmavad suvandeid *Täisarv*, *Reaalarv*, *Kahendmuutuja* ja *String*.

## <a name="paths"></a><a name="Paths"></a>Teed

Kui avaldis viitab struktureeritud andmeallikale, saate kasutada tee määratlemist, et valida selle andmeallika kindel primitiivne element. Punkti (.) kasutatakse struktureeritud andmeallika üksikute elementide eraldamiseks. Näiteks praegune ER-i mudelivastendus sisaldab andmeallikat **InvoiceTransactions**, mis annab vastuseks kirjete loendi. Kirje struktuur **InvoiceTransactions** sisaldab välju **AmountDebit** ja **AmountCredit**, mis mõlemad tagastavad arvulisi väärtusi. Seega saate arveldatud summa arvutamiseks koostada järgmise avaldise: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Konstruktsioon `InvoiceTransactions.AmountDebit` selles avaldises on tee, mida kasutatakse väljale **AmountDebit** juurdepääsemiseks andmeallikas **InvoiceTransactions** tüübis *Kirjete loend*.

### <a name="relative-path"></a>Suhteline tee

Kui struktureeritud andmeallika tee algab märgiga @, siis on see suhteline tee. @-märk kuvatakse kasutatava hierarhilise struktuuripuu absoluutse tee allesjäänud osa asemel. Järgmisel joonisel on toodud näide. Siin näitab absoluutne tee `Ledger.'accountingCurrency()'`, et arvestusvaluuta väärtus andmeallikast **Pearaamat** on sisestatud andmemudeli väljale **AccountingCurrency**.

![Absoluutse tee näide ER-i mudelivastenduse kujundaja lehel.](./media/ER-FormulaLanguage-AbsolutePath.png)

Järgmisel joonisel toodud näide näitab, kuidas kasutatakse suhtelist teed. Suhteline tee `@.AccountNum` näitab, et välja **AccountNum** andmeallikas **Intrastat** (mis ilmub andmemudeli hierarhilises puus üks tase väljast **AccountNum** üleval pool) kasutatakse kliendi või hankija kontonumbri sisestamiseks andmemudeli väljale **AccountNum**.

![Suhtelise tee näide ER-i mudelivastenduse kujundaja lehel.](./media/ER-FormulaLanguage-RelativePath1.png)

Absoluutse tee ülejäänud osa kuvatakse samuti [ER-i valemiredaktoris](general-electronic-reporting-formula-designer.md).

![Absoluutse tee ülejäänud osa ER-i valemi kujundaja lehel.](./media/ER-FormulaLanguage-RelativePath2.png)

Lisateabe saamiseks vt teemat [Suhtelise tee kasutamine ER-mudelite ja -vormingute andmesidemetes](relative-path-data-bindings-er-models-format.md).

## <a name="functions"></a><a name="Functions"></a>Funktsioonid

ER-i sisseehitatud funktsioone saab kasutada ER-i avaldistes. Kõiki avaldise konteksti (st praegune ER-i mudelivastendus või ER-i vorming) andmeallikaid saab kasutada helistamisfunktsioonide parameetritena vastavalt helistamisfunktsioonide käivitamine argumentide loendile. Konstante saab kasutada ka funktsioonide käivitamise parameetritena. Näiteks praegune ER-i mudelivastendus sisaldab andmeallikat **InvoiceTransactions**, mis annab vastuseks kirjete loendi. Kirje struktuur **InvoiceTransactions** sisaldab välju **AmountDebit** ja **AmountCredit**, mis mõlemad tagastavad arvulisi väärtusi. Seega saate arveldatud summa arvutamiseks koostada järgmise avaldise, mis kasutab sisseehitatud ER-i ümardamisfunktsiooni: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

ER-i mudelivastenduste ja ER-i aruannete koostamisel saate kasutada ER-i funktsioone järgmistest kategooriatest.

- [Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)
- [Loendi funktsioonid](er-functions-category-list.md)
- [Loogilised funktsioonid](er-functions-category-logical.md)
- [Matemaatilised funktsioonid](er-functions-category-mathematical.md)
- [Kirje funktsioonid](er-functions-category-record.md)
- [Tekstifunktsioonid](er-functions-category-text.md)
- [Andmete kogumise funktsioonid](er-functions-category-data-collection.md)
- [Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)
- [Tüübiteisenduse funktsioonid](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Funktsioonide loendi laiend

ER laseb laiendada nende funktsioonide loendit, mida kasutatakse ER-i avaldistes. Nõutav on mõni projekteerimise panus. Lisateabe saamiseks vt [Elektroonilise aruandluse (ER) funktsioonide loendi laiendamine](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Liitavaldised

Saate luua liitavaldisi, mis kasutavad erinevate kategooriate funktsioone, kui andmetüübid ühtivad. Kui kasutate funktsioone koos, vastendage väljundi andmetüüp ühest funktsioonist teise funktsiooni nõutud sisendi andmetüübi jaoks. Näiteks võimaliku „Loend on tühi” tõrke vältimiseks ER-i vormingu elemendile välja sidumisel, kombineerige funktsioone kategooriast [Loend](er-functions-category-list.md) koos kategooria [Loogiline](er-functions-category-logical.md) funktsioonidega, nagu järgmises näites on toodud. Siin kasutab valem funktsiooni [IF](er-functions-logical-if.md), et katsetada, kas loend **IntrastatTotals** on tühi, enne kui see tagastab sellest loendist nõutava kogumi väärtuse. Kui loend **IntrastatTotals** on tühi, tagastab valem väärtuse **0** (null).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Mitu lahendust

Sageli saate sama teabe teisenduse tulemuse mitmel viisil, kasutades erinevate kategooriate funktsioone või sama kategooria erinevaid funktsioone. Näiteks eelneva avaldise saab konfigureerida ka funktsiooniga [COUNT](er-functions-list-count.md) kategooriast [Loend](er-functions-category-list.md).

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse funktsioonide loendi laiendamine](general-electronic-reporting-formulas-list-extension.md)

[Primitiivseid andmetüüpe toetab](er-formula-supported-data-types-primitive.md)

[Toetatud liitandmetüübid](er-formula-supported-data-types-composite.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
