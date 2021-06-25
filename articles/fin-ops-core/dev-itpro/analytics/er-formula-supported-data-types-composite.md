---
title: Elektroonilise aruandluse valemite toetatud liitandmetüübid
description: See teema annab teavet liitandmetüüpide kohta, mida toetatakse elektroonilises aruandluses (ER) valemites.
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ed9e62751b6be9fad6de3bf262d37d7977d192
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224086"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Elektroonilise aruandluse valemite toetatud liitandmetüübid

[!include [banner](../includes/banner.md)]

See teema annab teavet liitandmetüüpide kohta, mida toetatakse [elektroonilises aruandluses (ER)](general-electronic-reporting.md) valemites. Liitandmetüübid on [klass](#class), [konteiner](#container), [kirje](#record), [kirje loend](#record-list), ja [objekt](#object).

## <a name="class"></a><a name="class"></a>Klass

*Klass* andmetüüp viitab avaliku rakenduse klassile. ER-is on see esitatud kirjena, mis on [*kirje*](#record) mis sisaldab eraldi välja iga viidatud klassi avaliku meetodi jaoks. Kui meetodi kutse on parameetritega seadistatud, peate meetodi kutsumiseks konfigureeritud ER-avaldises määrama ka vajalike tüüpide nõutavad argumendid.

ER-i [vastendamise](general-electronic-reporting.md#data-model-and-model-mapping-components) ja [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponentide puhul saate lisada **klassi** andmeallika, mis on esitatud andmeallikana ja annab tulemuseks *klassi* tüüp. See andmeallikas sisaldab klassi avalikuid meetodeid, mida saab käivitada käitusajal.

> [!NOTE]
> ER-avaldistest saab kutsuda ainult meetodeid, mis tagastavad väärtuse.
>
> ER-avaldistest saab kutsuda ainult meetodeid, mille vahemik on null kuni kaheksa argumenti.

*Klassi* vaikeväärtuseks on **tühi**.

Järgmine näide näitab, kuidas klassitüübi **süsteemiteave(xinfo)** **klass** tüüpi andmeallikas lisatakse, et muuta **xinfo** rakenduse klassi eksemplar ja kutsuda sea käesoleva rakenduse nime saamiseks **tooteNimi()**. Praeguse rakenduse nimi toodetakse käitusajal, käivitades sidumise `xInfo.productName`, mis oli konfigureeritud ER andmemudeli **Rakenduse nimi(RakenduseNimi)** andmemudeli väljale. See sidumine kutsub käesoleva mudeli vastendamises esitatud **xInfo** rakenduse klassi `productName()` meetodit  **süsteemiteabe(xInfo)** andmeallikana.

[![Klassi andmeallikas konfigureerimine ER-i mudeli vastenduse koostajas](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Järgmine näide näitab, kuidas ER-vorming konfigureeritakse antud rakenduse nime panemiseks loodud dokumentidesse. Kasutatud andmemudeli **Tarkvaranime (Tarkvaranimi)** väli oli seotud **stringi** komponendiga, mis on pesastatud **kasutatud rakendus** ER-vormingu XML-elemendi alla. Seega paigutatakse praeguse rakenduse nimi käitusajal XML-vormingus XML-elementi loodud dokumenti **kasutatud rakendus**.

[![Elektroonilise väljamineva dokumendi struktuuri konfigureerimine ER-vormingu kujundaja](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Konteiner

*Konteiner* andmetüüp sisaldab binaarsisu. *Konteiner* väärtust saab kasutada kindla teabe salvestamisest loodud dokumenddi edastamiseks. ER-i raamistikus kasutatakse seda andmetüüpi sageli meediasisu panemiseks, nt ettevõtte logo loodud dokumentidesse.

> [!NOTE]
> Kuigi iga meediaüksust saab esitada *konteineri* väärtusena, ei tähista iga *konteineri* väärtus meediakaupa. Seega, kui konfigureerite ER-vormingu nii, et see kasutab *konteinerit* pildi paigutamiseks loodud dokumentidesse, kuid viidatud *konteiner* ei tagasta meediumisisu, võib välja arvata erandi, mis sarnaneb järgmise näitega: "Vea täitmiskood: Binaar (objekt), meetod constructFromContainer kutsuti kehtetute parameetritega."

*Konteineri* vaikeväärtuseks on **tühi**.

Järgmine näide näitab, kuidas **rasterpilt(pilt)** *Konteiner* tüüpi väli on seotud andmemudeli **logo** väljal, mille tüübiks on **konteiner** **Müügiarve** mudeli vastendamisel. Selline sidumine muudab ettevõtte logo kättesaadavaks mis tahes ER-vormingus, mis on loodud **Müügiarve** juurdefinitsiooni jaoks ja mis kasutab seda mudelivastendamist käitusajal.

[![Konteineritüübi välja sidumine ER-mudeli vastendamise kujundajaga](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Salvestamine

*Kirje* on nimetatud väljade kogum, millest igaüks on seotud kas [primitiivse](er-formula-supported-data-types-primitive.md) andmetüübi või liitandmetüübi väärtusega. Tavaliselt kasutatakse *kirjet* kirjeloendi üksiku kirje tähistamiseks. Sel juhul näitab iga kaup üksikuid välju, meetodeid ja suhteid.

*Kirje* vaikeväärtuseks on **tühi**.

> [!NOTE]
> Tühja *kirje* välja väärtuse toomisel tagastatakse vastava andmetüübi vaikeväärtus.

*Kirje* on võimalik saada järgmiste funktsioonide abil:

- [ESIMENE](er-functions-list-first.md)
- [ESIMENEVÕINULL](er-functions-list-firstornull.md)
- [TÜHIKIRJE](er-functions-record-emptyrecord.md)
- [NULLKONTEINER](er-functions-record-nullcontainer.md)

Lisateavet *kirje* väärtuste teisendamise kohta vt [loendikategooria ER-funktsioonide loenist](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Kirjete loend

*Kirjeloend* on *kirje* tüüpi kaupade loend. Tavaliselt kasutatakse *kirjeloendi* andmebaasi tabelist toodud kirjete loendi tähistamiseks.

Vaikimisi pääseb *kirjeloendi* kirjetele järjestikku. Konkreetsele kirjele juurdepääsuks saate kasutada [INDEX](er-functions-list-index.md) funktsiooni ja määrata *täisarvu* indeksi.

*Kirjeloendi* vaikeväärtuseks on **tühi**. Saate kasutada [ISEMPTY](/er-functions-list-isempty.md) funktsiooni, et hinnata, kas *kirjeloend* on tühi.

> [!NOTE]
> Kui *kirjeloend* on tühi, õhjustab mis tahes katse selles saada välja väärtus selle *kirje* jaoks käitusajal erandilt. Teavet selle kohta, kuidas aitab vältida seda tüüpi käitusaja erandeid, vt [tühjade loendijuhtumitega arvestamine](er-components-inspections.md#i9).

*Kirjeloend* on võimalik saada järgmiste funktsioonide abil:

- [KÕIKÜKSUSED](er-functions-list-allitems.md)
- [KÕIGIÜKSUSTEPÄRING](er-functions-list-allitemsquery.md)
- [TÜHILOEND](er-functions-list-emptylist.md)
- [LOEND](er-functions-list-list.md)
- [ERISUSTELOEND](er-functions-list-listdistinct.md)

Lisateavet *kirje loendi* väärtuste teisendamise kohta vt [loendikategooria ER-funktsioonide loendist](er-functions-category-list.md). Selleks, et teada saada, kuidas *kirjelonedi* üksusi tutvustada, täitke need rakendusandmetega ja kasutage seejärel andmeid äridokumentide loomiseks [vt kohandatud aruande printimiseks uue ER-lahenduse loomine](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Objekt

*Objekt* viitab *klassi* olekulisele eksemplarile. Tavaliselt algatatakse *objekt* lähtekoodis. See edastatakse seejärel ER-mudeli vastendamisse ja annab täitmiskonteksti üksikasjad.

*Objekti* vaikeväärtuseks on **tühi**.

Järgmine näide näitab, kuidas objektitüübi **ReportDataContakti** andmeallikas lisatakse *Objekti* tüüpi loodud arve teabe edastamiseks lähtekoodist **Projekti arve** muddeli vastendamisel. Näiteks arveeksemplari tekst edastatakse täitmiskonteksti osana. See tekst võetakse lähtekoodist käitusajal, käivitades `ReportDataContract.parmInvoiceInstanceText` ER-i andmemudeli **märkuse** välja jaoks konfigureeritud sidumise. See sidumine kutsub `parmInvoiceInstanceText()` meetodit **PSAProjArveLeping** rakenduse klassis, mis esindab käesoleva mudeli vastendamises esitatud **ReportDataContrac** andmeallikat.

[![Objekti andmeallika konfigureerimine ER-i mudeli vastenduse koostajas](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Teavet selle kohta, kuidas edastada täitmiskonteksti üksikasju lähtekoodist jooksvale ER-lahendusele, vt ["Rakenduste arendamise faktid, et kutsuda kujundamisaruannet](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse valemi keel](er-formula-language.md)
- [Primitiivseid andmetüüpe toetab](er-formula-supported-data-types-primitive.md)
