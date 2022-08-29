---
title: Kujundage ER-vorming Excelis genereeritud dokumentide saalimiseks
description: See artikkel selgitab, kuidas kujundada elektroonilise aruandluse (ER) vormingut, milles loodud dokument saalitakse Microsoft Excel.
author: kfend
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: EROperationDesigner
ms.openlocfilehash: e4a34dffda9e9b95f5d6c7ee382723663817ec6b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284997"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>Kujundage ER-vorming Excelis genereeritud dokumentide saalimiseks

[!include [banner](../includes/banner.md)]

See artikkel selgitab, [kuidas kasutaja süsteemiadministraatoris või elektroonilise aruandluse funktsiooninõustaja rollis saab konfigureerida elektroonilise aruandluse (ER)](general-electronic-reporting.md)Microsoft Excel vormingu väljaminevate dokumentide loomiseks ja dokumendi saalimise haldamiseks.

Selles näites muudate Microsofti esitatud ER-vormingut, mida kasutatakse kontrollaruande printimiseks Intrastat-deklaratsiooni [loomisel](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Selle aruandega saate jälgida aruandes esitatud Intrastati kandeid. Teie muudatusted lubavad teil hallata loodud kontrollaruannete lehekülgede saalimist.

Selle artikli protseduurid saab DEMF-ettevõttes **lõpule** viia. Koodi pole vaja kirjutada. Enne alustamist laadige alla ja talletage kohalikult järgmised failid.

| Kirjeldus       | Faili nimi |
|-------------------|-----------| 
| Aruandemall 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Aruandemall 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>ER-raamistiku konfigureerimine

Minimaalsete [ER-i parameetrite konfigureerimine](er-quick-start2-customize-report.md#ConfigureFramework), mis on vajalikud ER-i raamistiku kasutamiseks. Enne ER-raamistiku kasutamist standardse ER-vormingu kohandatud versiooni loomiseks peate selle häälestuse lõpule viima.

## <a name="import-the-standard-er-format-configuration"></a>Standardse ER‑vormingu konfiguratsiooni importimine

Järgige standardse ER-vormingu [konfiguratsiooni importimise etappe](er-quick-start2-customize-report.md#ImportERSolution1), et lisada praegusele Dynamics 365 Finance’i eksemplarile standardsed ER-konfiguratsioonid. Importige **Intrastati aruande** vormingu konfiguratsiooni versioon **1.9**. **Intrastati põhimudeli** konfiguratsiooni baasversioon 1 imporditakse automaatselt hoidlast.

## <a name="customize-the-standard-er-format"></a>Standardse ER-vormingu kohandamine

### <a name="create-the-custom-er-format"></a>Kohandatud ER-vormingu loomine

Selles stsenaariumis olete te Litaware, Inc. esindaja, kes on praegu valitud aktiivse ER-i konfiguratsiooni pakkujaks. Peate looma uue ER-vormingu konfiguratsiooni, kasutades alusena **Intrastat-aruande** konfiguratsiooni.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Intrastat mudel** ja valige **Intrastat aruanne**. Litware, Inc. kasutab kohandatud versiooni alusena selle ER-vormingu konfiguratsiooni versiooni 1.9.
3. Rippmenüü dialoogiboksi avamiseks valige käsk **Loo konfiguratsioon**. Selle dialoogiboksi abil saate luua uue konfiguratsiooni kohandatud maksevormingu jaoks.
4. Valige väljagrupis **Uus** suvand **Tuleta nimest: Intrastat aruanne, Microsoft**.
5. Väljale **Nimi** sisestage **Intrastati aruanne Litware**.
6. Konfiguratsiooni loomiseks valige **Loo konfiguratsioon**.

Luuakse ER-vormingu konfiguratsiooni **Intrastat aruanne Litware** versioon 1.9.1. Selle versiooni olek on Mustand **ja** seda saab redigeerida. Teie kohandatud ER-vormingu praegune sisu vastab Microsofti antud vormingu sisule.

### <a name="make-the-custom-format-runnable"></a>Kohandatud vormingu tegemine käitatavaks

Kui teie kohandatud vormingu esimene versioon on loodud ja selle olek on **Mustand**, saate vormingu käitada testimise eesmärgil. Aruande käitamiseks peate töötlema hankija makset makseviisi abil, mis viitab teie kohandatud ER-vormingule. Kui kutsute rakendusest ER-vormingu, kaalutakse vaikimisi ainult versioone, mille olek on **Lõpetatud** **või** Ühiskasutuses. Selle käitumise abil saab vältida ER-vormingute kasutamist, mille koostamine on lõpetamata. Kuid oma testikäivitustel saate sundida rakendust kasutama teie ER-vormingu versiooni, mille olekuks on **Mustand**. Sedasi saate korrigeerida praeguse vormingu versiooni, kui muudatusi on vaja. Lisateavet vt jaotisest [Kohaldatavus](electronic-reporting-destinations.md#applicability).

ER-vormingu mustandversiooni kasutamiseks peate ER-vormingu selgelt märgistama.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Seadke dialoogiboksis **Kasutaja parameetrid** suvandi **Käivitamissätted** väärtuseks **Jah** ja valige seejärel **OK**.
4. Vastavalt vajadusele valige **Redigeeri**, et muuta praegune leht redigeeritavaks.
5. Valige vasakpoolse paani konfiguratsioonipuus suvand **Intrastat aruanne Litware**.
6. Seadke suvandi **Käivita mustand** väärtuseks **Jah** ning valige seejärel **Salvesta**.

    ![Suvand Käivita mustand Konfiguratsioonide lehel.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Väliskaubanduse parameetrite seadistamine kohandatud ER-vormingu kasutamiseks

Järgige neid samme väliskaubanduse parameetrite konfigureerimiseks, et kasutada kohandatud vormingut.

1. Avage **Maksud** \> **Seadistus** \> **Väliskaubandus** \> **Väliskaubanduse parameetrid**.
2. **Väliskaubanduse parameetrid** lehel, **Elektrooniline aruandlus** Kiirkaardil, väljal **Failivormingu vastendamine** valige **Intrastati aruanne Litware**.
3. Väljal **Aruandevormingu vastendamine** valige **Intrastati aruanne Litware**.
4. Valige käsk **Salvesta**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Kohandatud vormingu konfigureerimine allalaaditud aruandemalli kasutamiseks

### <a name="review-the-first-downloaded-excel-template"></a>Vaadake üle esimene allalaaditud Exceli mall

1. Avage Exceli töölauarakenduses mailifail **ERIntrastatReportDemo1.xlsx**, mille varem alla laadisite.
2. Kontrollige, kas mall sisaldab nimevahemikeid loodud dokumentide aruande päise, aruande üksikasjade ja jaluse sektsioonide loomiseks.

    ![Exceli malli 1 paigutus töölauarakenduses.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Praeguse Exceli malli asendamine kohandatud ER-vormingus

Peate kohandatud ER-vormingusse lisama uue Exceli malli.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Intrastat mudel** \> **Intrastat aruanne** ja valige **Intrastat aruanne Litware** konfiguratsioon.
3. Valige **Kujundaja**.
4. Valige lehe **Vormingu koostaja** toimingupaanil suvand **Näita üksikasju**.
5. Kontrollige, kas **Intrastat: Exceli** juurvormingu komponent on valitud, ja seejärel valige tegevuspaani vahekaardi **Importimine** jaotises **Importimine** suvand **Uuenda Excelist**.
6. Valige **Värskenda Excelist** dialoogiboksis **Värskenda malli**.
7. Dialoogiboksis **Avatud** sirvige ja valige varem alla laaditud fail **ERIntrastatReportDemo1.xlsx** ja seejärel valige **Ava**.
8. Valige nupp **OK**.
9. Valige käsk **Salvesta**.

![Vormingu struktuur ER-vormingukujundajas pärast uue Exceli malli lisamist.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Muutke andmete sidumist, et näidata loodud aruandes kauba kirjeldust.

1. Valige lehel **Vormingu kujundaja** vahekaart **Vastendamine**.
2. Laiendage **Intrastati** \> **Aruande read** ja valige **Kaubaartikli koodi** komponent.
3. Valige **Valemi redigeerimine**.
4. Muutke sidumisvalem `@.CommodityCode` valemiks `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Valige käsk **Salvesta**.

![Konfigureeritud sidumine kauba kirjelduse näitamiseks ER-vormingu kujundajas.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Intrastati deklaratsiooni kontrollaruande koostamine

Esmalt kontrollige, et Intrastati kanded on **Intrastati** lehel aruandluseks.

![Ülekanded Intrastati lehel.](./media/er-paginate-excel-reports-transactions1.gif)

Seejärel kasutage kohandatud ER-vormingut Intrastati deklaratsiooni kontrollaruande loomiseks.

1. Avage **Maks** \> **Deklaratsioonid** \> **Väliskaubandus** \> **Intrastat**.
2. Valige lehel **Intrastat** toimingute paanil **Väljund** \> **Aruanne**.
3. Dialoogiboksis **Intrastati aruanne** järgige järgmisi samme aruande käivitamiseks:

    1. Seadistage väljad **Alates** ja **Kuni**, et kaasata aruandesse kindlad Intrastati kanded.
    2. Määrake suvand **Loo fail** valikule **Ei**.
    3. Määrake suvand **Loo aruanne** valikule **Jah**.
    4. Valige nupp **OK**.

4. Laadige alla ja salvestage loodud dokument.
5. Avage dokument Excelis ja vaadake see üle.

    ![Genereeritud Exceli dokument töölaua rakenduses.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Kohandatud vormingu konfigureerimine loodud dokumentide lehekülgedeks saalimiseks

### <a name="review-the-second-downloaded-excel-template"></a>Vaadake üle teine allalaaditud Exceli mall

1. Avage Excelis mailifail **ERIntrastatReportDemo2.xlsx**, mille varem alla laadisite.
2. Võrrelge seda malli **ERIntrastatReportDemo1.xlsx** malliga ja kontrollige, et see sisaldab mitut uut Exceli nime, mida luua ja täita leheküljespetsiifilisi jaotisi loodud dokumentides:

    - Aruande lehekülje päiste loomiseks lisatakse vahemik **ReportPageHeader**.
    - Aruande lehekülje jaluste loomiseks lisatakse vahemik **ReportPageFooter**.
    - Lahter **ReportPageFooter\_PageLines** on konfigureeritud kuvama kannete arvu lehel.
    - Lahter **ReportPageFooter\_PageAmount** on konfigureeritud kuvama kannete koguarvu lehel.
    - Lahter **ReportPageFooter\_PageWeight** on konfigureeritud kuvama kannete kaalu lehel.
    - Lahter **ReportPageFooter\_RunningCounterLines** on konfigureeritud kuvama kannete jooksvat loendurit aruande algusest praeguse lehekülje kaudu.
    - Lahter **ReportPageFooter\_RunningTotalAmount** on konfigureeritud näitama kõigi tehingute jooksvat summat aruande algusest kuni praeguse leheni.
    - Lahter **ReportPageFooter\_RunningTotalWeight** on konfigureeritud näitama tehingute jooksvat kaalu aruande algusest kuni praeguse leheni.

    ![Exceli malli 2 paigutus töölauarakenduses.](./media/er-paginate-excel-reports-template2a.gif)

    Selle malli lahter **CommodityCode** on konfigureeritud lahtriteksti vormindama. Kuna kande üksikasjade rida on konfigureeritud nii, et see sobiks automaatselt rea kõrgusega, peab terve rea kõrgus automaatselt muutuma, kui välja **CommodityCode** lahter sisaldab teksti.

    ![Lahtriteksti vormindamiseks konfigureeritud lahter CommodityCode.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Korrake praeguse Exceli malli asendamist kohandatud ER-vormingus

1. Järgige selle artikli kohandatud [ER-vormingu sektsioonis praeguse Exceli malli](#replace-template) asendamise etappe. Kuid sammus 7 valige fail **ERIntrastatReportDemo2.xlsx**.
2. Lehel **Vormingu kujundaja** valige laienda **Intrastat**.
3. Nimetage [Vahemiku](er-fillable-excel.md#range-component) vormingu komponendid, mis on lisatud redigeeritavasse ER-vormingusse, et sünkroonida struktuur rakendatud Exceli malli struktuuriga:

    1. Valige **Vahemiku** komponent, mis on seostatud Exceli nimega **ReportPageHeader**.
    2. Sisestage vahekaardi **Vorming** väljale **Nimi** **Aruandelehe päis**.
    3. Valige **Vahemiku** komponent, mis on seostatud Exceli nimega **ReportPageFooter**.
    4. Sisestage vahekaardi **Vorming** väljale **Nimi** **Aruandelehe jalus**.

4. Valige käsk **Salvesta**.

![Vormingu struktuur ER-vormingukujundajas pärast Exceli malli asendamist.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Muuda vormingu struktuuri dokumendi lehekülgede saalimise juurutamiseks

1. Valige **Vormingukujundaja** lehel vasakul paanil olevas vormingupuus **Intrastati** juurkomponent.
2. Valige **Lisa**.
3. Valige dialoogiboksis **Lisa** komponentide rühmas **Excel** komponent [Page](er-fillable-excel.md#page-component).
4. Sisestage dialoogiboksi **Komponendi atribuut** väljale **Nimi** sisestage **Aruande leht**. Seejärel valige **OK**.
5. **Aruandelehe päise** komponendi kasutamiseks lehekülje päisena igal loodud lehel järgige neid samme:

    1. Valige **Aruandelehe päise** komponent ja seejärel suvand **Lõika**.
    2. Valige **Aruandelehe päise** komponent ja seejärel suvand **Kleebi**.
    3. Laienda **Aruandeleht**.
    4. Et **Lehekülje** komponent seda vahemikku lehekülje päisena [arvestaks](er-fillable-excel.md#page-component-structure), valige **Aruandelehe päis** ja seejärel valige vahekaardi **Vorming** väljal **Andmeedastussuund** suvand **Andmeedastuse ei toimu**.

6. Loodud dokumendi lehekülgedeks saalimiseks nii, et aruande ridade sisu peetakse arvesse, järgige neid samme:

    1. Valige **Aruande joonte** komponent ja seejärel suvand **Lõika**.
    2. Valige **Aruandelehe päise** komponent ja seejärel suvand **Kleebi**.

7. Aruande jaluse kaasamiseks aruande ridade järele, kuid enne lõpplehe jalusesse, järgige neid samme:

    1. Valige **Aruande jaluse** komponent ja seejärel suvand **Lõika**.
    2. Valige **Aruandelehe päise** komponent ja seejärel suvand **Kleebi**.

8. **Aruandelehe jaluse** komponendi kasutamiseks lehekülje jalusena igal loodud lehel järgige neid samme:

    1. Valige **Aruandelehe jaluse** komponent ja seejärel suvand **Lõika**.
    2. Valige **Aruandelehe päise** komponent ja seejärel suvand **Kleebi**.
    3. Et **Lehekülje** komponent seda vahemikku lehekülje jalusena [arvestaks](er-fillable-excel.md#page-component-structure), valige **Aruandelehe jalus** ja seejärel valige vahekaardi **Vorming** väljal **Andmeedastussuund** suvand **Andmeedastuse ei toimu**.

![Vormingu struktuur ER-vormingukujundajas pärast dokumendi lehekülgede rakendamist.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Andmeallikate lisamine lehe jaluse kogusummade arvutamiseks

Lehekülje kogusumma arvutamiseks, jooksvate loendurite ja jooksvate koguväärtuste arvutamiseks tuleb konfigureerida uued andmeallikad ning need lehekülje jaluse jaotises kuvama. Me soovitame selleks otstarbeks kasutada [Andmete kogumine](er-data-collection-data-sources.md) andmeallikaid.

1. Valige lehel **Vormingu kujundaja** vahekaart **Vastendamine**.
2. Valige uuesti käsk **Lisa juur** ja tehke järgmist:

    1. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Üldine** suvand **Tühi konteiner**.
    2. Sisestage dialoogiboksi **"Tühi konteiner" andmeallika atribuudid** väljale **Nimi** väärtus **Kokku**.
    3. Valige nupp **OK**.

3. Valige andmeallika **Kogum**, valige **Lisa** ja järgige seejärel neid samme:

    1. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Üldine** suvand **Tühi konteiner**.
    2. Sisestage dialoogiboksi **"Tühi konteiner" andmeallika atribuudid** väljale **Nimi** väärtus **Leht**.
    3. Valige nupp **OK**.

4. Valige uuesti käsk **Lisa** ja tehke järgmist.

    1. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Üldine** suvand **Tühi konteiner**.
    2. Sisestage dialoogiboksi **"Tühi konteiner" andmeallika atribuudid** väljale **Nimi** väärtus **Toimib**.
    3. Valige nupp **OK**.

5. Valige **Kokku.Leht** andmeallikas, valige **Lisa** ja järgige seejärel neid samme:

    1. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Funktsioonid** suvand **Andmekogum**.
    2. Sisestage dialoogiboksi **"Andmekogum" andmeallika atribuudid** väljale **Nimi** väärtus **Kogus**.
    3. Väljal **Üksuse tüüp** valige **Tegelik**.
    4. Seadke **Kõikide väärtuste kogumine** väärtuseks **Jah**.
    5. Valige nupp **OK**.

6. Valige uuesti käsk **Lisa** ja tehke järgmist.

    1. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Funktsioonid** suvand **Andmekogum**.
    2. Sisestage dialoogiboksi **"Andmekogum" andmeallika atribuudid** väljale **Nimi** väärtus **Kaal**.
    3. Väljal **Üksuse tüüp** valige **Tegelik**.
    4. Seadke **Kõikide väärtuste kogumine** väärtuseks **Jah**.
    5. Valige nupp **OK**.

7. Valige **Total.Running** andmeallikas, valige **Lisa** ja järgige seejärel neid samme:

    1. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Funktsioonid** suvand **Andmekogum**.
    2. Sisestage dialoogiboksi **"Andmekogum" andmeallika atribuudid** väljale **Nimi** väärtus **Kogus**.
    3. Väljal **Üksuse tüüp** valige **Tegelik**.
    4. Seadke **Kõikide väärtuste kogumine** väli väärtuseks **Jah**.
    5. Valige nupp **OK**.

8. Valige uuesti käsk **Lisa** ja tehke järgmist.

    1. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Funktsioonid** suvand **Andmekogum**.
    2. Sisestage dialoogiboksi **"Andmekogum" andmeallika atribuudid** väljale **Nimi** väärtus **Kaal**.
    3. Väljal **Üksuse tüüp** valige **Tegelik**.
    4. Seadke **Kõikide väärtuste kogumine** väli väärtuseks **Jah**.
    5. Valige nupp **OK**.

9. Valige uuesti käsk **Lisa** ja tehke järgmist.

    1. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Funktsioonid** suvand **Andmekogum**.
    2. Sisestage dialoogiboksi **"Andmekogum" andmeallika atribuudid** väljale **Nimi** väärtus **Read**.
    3. Valige väljalt **Kauba tüüp** suvand **Integer**.
    4. Seadke **Kõikide väärtuste kogumine** väli väärtuseks **Jah**.
    5. Valige nupp **OK**.

10. Valige käsk **Salvesta**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Lisage andmeallikaid lehe jaluse nähtavuse juhtimiseks

Kui plaanite kontrollida lehe jaluse nähtavust ja te ei plaani kaasata lõpplehele jaluset, kui see sisaldab kandeid, konfigureerige uus andmeallikas, et arvutada nõutav jooksev loendur.

1. Valige lehel **Vormingu kujundaja** vahekaart **Vastendamine**.
2. Valige **Total.Running** andmeallikas ja klõpsake käsku **Lisa**.
3. Valige dialoogiboksis **Andmeallika lisamine** jaotises **Funktsioonid** suvand **Andmekogum**.
4. Sisestage dialoogiboksi **"Andmekogum" andmeallika atribuudid** väljale **Nimi** väärtus **Read2**.
5. Valige väljalt **Kauba tüüp** suvand **Integer**.
6. Seadke **Kõikide väärtuste kogumine** väärtuseks **Jah**.
7. Valige nupp **OK**.
8. Valige käsk **Salvesta**.

![Lisatud andmeallikad ER-vormingu kujundajasse.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Koguväärtuste kogumiseks sidumiste konfigureerimine

1. **Vormingukujundaja** lehel laiendage vormingupuus **Aruanderidade** komponenti ja valige pesastatud **arve väärtuse** komponent.
2. Valige **Valemi redigeerimine**.
3. Muutke sidumisvalem `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` valemiks `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Lisaks summa väärtuse lisamisele iga iteereeritud kande jaoks Exceli lahtrisse kogub see sidumine väärtust andmekogumis **Total.Page.Amount** andmeallikas.

4. Valige pesastatud **kaalu** komponent.
5. Valige **Valemi redigeerimine**.
6. Muutke sidumisvalem `@.'$RoundedWeight'` valemiks `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Lisaks kaalu väärtuse lisamisele iga iteereeritud kande jaoks Exceli lahtrisse kogub see sidumine väärtust andmekogumis **Total.Page.Weight** andmeallikas.

![Konfigureeritud sidumised koguväärtuste kogumiseks ER-vormingu kujundajasse.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Lehe jaluse kogusummade täitmiseks sidumiste konfigureerimine

1. **Vormingukujundaja** lehel laiendage vormingupuus **Aruandelehe jaluse** komponenti, valige pesastatud **Vahemiku** komponent, mis viitab lahtrile Excel **ReportPageFooter\_PageAmount** ja järgige seejärel neid samme:

    1. Valige parempoolsel paanil andmeallikate puul üksus **Total.Page.Amount.Sum()**.
    2. Valige **Seo**.
    3. Valige **Valemi redigeerimine**.
    4. Valemi uuendamine `Total.Page.Amount.Sum(false)` valemiks.

    > [!NOTE]
    > Selle funktsiooni argumendi väärtuseks tuleb määrata **Väär**, et koguda kogutud andmeid praeguse lehekülje kohta, sest see teave on vajalik käitatava summa, iga lehe ridade koguarvu ja ridade loenduri arvutamiseks.

2. Valige vormingupuus exceli lahtrile **ReportPageFooter\_PageWeight** viitav pesastatud **Vahemiku** komponent ja järgige seejärel neid samme:

    1. Valige parempoolsel paanil andmeallikate puul üksus **Total.Page.Weight.Sum()**.
    2. Valige **Seo**.
    3. Valige **Valemi redigeerimine**.
    4. Valemi uuendamine `Total.Page.Weight.Sum(false)` valemiks.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Seadistuste seadistamine lehe jooksvate kogusummade täitmiseks

1. **Vormingu kujundaja** lehel laiendage vormingupuus **Aruandelehe jaluse** komponenti, valige pesastatud **Vahemiku** komponent, mis viitab lahtrile Excel **ReportPageFooter\_RunningTotalAmount** ja järgige seejärel neid samme:

    1. Valige parempoolsel paanil andmeallikate puul üksus **Total.Running.Amount.Collect()**.
    2. Valige **Seo**.
    3. Valige **Valemi redigeerimine**.
    4. Valemi uuendamine `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` valemiks.

    > [!NOTE]
    > Operand `Total.Running.Amount.Sum(false)` tagastab eelnevalt kogutud kogusumma. Operand `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` tagastab praeguse lehekülje kogusumma. Peate määrama teise operandi pesastatud funktsiooni argumendi väärtuseks **Tõene**, et lähtestada `Total.Page.Amount` andmete kogum kohe, kui see väärtus on `Total.Running.Amount` kogumisse asetatud. Määratud argument peab alustama järgmise lehe kogusumma kogumist 0 (null) väärtusest.
    >
    > `Total.Running.Amount.Sum(false)` funktsiooni kutsutakse jooksva lehe lahtri Excel **ReportPageFooter\_RunningTotalAmount** kogusumma sisestamiseks.

2. Valige vormingupuus exceli lahtrile **ReportPageFooter\_RunningTotalWeight** viitav pesastatud **Vahemiku** komponent ja järgige seejärel neid samme:

    1. Valige parempoolsel paanil andmeallikate puul üksus **Total.Running.Weight.Collect()**.
    2. Valige **Seo**.
    3. Valige **Valemi redigeerimine**.
    4. Valemi uuendamine `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))` valemiks.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Seadistuste seadistamine lehe jooksuloenduri täitmiseks

1. **Vormingu kujundaja** lehel laiendage vormingupuus **Aruandelehe jaluse** komponenti ja valige pesastatud **Vahemiku** komponent, mis viitab lahtrile Excel **ReportPageFooter\_RunningCounterLines**.
2. Valige **Valemi redigeerimine**.
3. Lisa `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))` valem.

    > [!NOTE]
    > See valem tagastab kogutud summaväärtuste arvu terve aruande kohta. See arv võrdub praegusel hetkel iteereeritud kannete arvuga. Samal ajal kogub valem tagastatud väärtuse kogumisse **Total.Running.Lines**.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Seadistuste seadistamine lehe jaluse loenduri täitmiseks

1. **Vormingu kujundaja** lehel laiendage vormingupuus **Aruandelehe jaluse** komponenti ja valige pesastatud **Vahemiku** komponent, mis viitab lahtrile Excel **ReportPageFooter\_PageLines**.
2. Valige **Valemi redigeerimine**.
3. Lisa `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)` valem.

    > [!NOTE]
    > See valem arvutab kannete arvu praegusel lehel erinevusena kannete arvu vahel, mis koguti kogu **Total.Page.Amount.Result** aruande kohta ja kannete arvu vahel, mis on talletatud selles etapis **Total.Running.Lines.Sum**. Kuna praeguse lehe kannete arv on talletatud **Total.Running.Lines** komponendi **Vahemiku** sidumisel, mis viitab lahtrile Excel **ReportPageFooter\_RunningCounterLines**, mis ei ole praegusel lehel veel kannete arvu kaasatud. Seetõttu võrdub see erinevus praegusel lehel tehtud kannete arvuga.

![Konfigureeritud sidumised lehe jaluseloenduri täitmiseks ER-vormingu kujundajas.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Komponentide nähtavuse konfigureerimine

Saate muuta lehekülje päise ja jaluse nähtavust konkreetsel loodud dokumendi leheküljel, et peita järgmised elemendid:

- Esimese lehe päis, sest aruande päis sisaldab juba veeru tiitleid
- Lehe päis igal lehel, millel pole viimase lehe puhul toimuvaid tehinguid
- Lehe jalus igal lehel, millel pole viimase lehe puhul toimuvaid tehinguid

Nähtavuse muutmiseks värskendage **Aruande lehe päise** ja **Aruande lehe jaluse** komponentide atribuuti **Lubatud**.

1. **Vormingu kujundaja** lehel laiendage vormingupuus **Aruande lehe** komponenti ja valige pesastatud **Aruande lehe päise** komponent, seejärel järgige neid samme:

    1. Valige **Muuda** välja **Lubatud** jaoks.
    2. Sisestage lehel **Valemikujundaja** väljale **Valem** järgmine avaldis:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Valige vormingupuus pesastatud **Aruandelehe jaluse** komponent ja järgige seejärel neid samme:

    1. Valige **Muuda** välja **Lubatud** jaoks.
    2. Sisestage lehel **Valemikujundaja** väljale **Valem** järgmine avaldis:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` konstruktsiooni kasutatakse kannete arvu arvutamiseks praegusel lehel. `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` konstruktsiooni kasutatakse praegusel lehel kannete arvu lisamiseks kogusse, et käsitleda õigesti järgmise lehekülje jaluse nähtavust.
    >
    > `Total.Running.Lines` kogumeid ei saa siin uuesti kasutada, kuna aluskomponendi atribuuti **Lubatud** töödeldakse **pärast** pesastatud komponentide sidumiste töötlemist. Kui atribuut **Lubatud** on töödeldud, on `Total.Running.Lines` kogum juba suurendatud praegusel lehel oleva kande arvu järgi.

3. Valige käsk **Salvesta**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Intrastati deklaratsiooni kontrollaruande koostamine (uuendatud)

1. Veenduge, et teie **Intrastat** lehel on 24 tehingut. Korrake selle artikli intrastati [deklaratsiooni kontrollaruande loomise](#generate-intrastat-control-report) jaotise samme kontrollaruande loomiseks ja ülevaatamiseks.

    Kõik kanded esitatakse esimesel lehel. Lehe kogusummad ja loendurid võrduvad aruande kogusummade ja loenduritega. Lehe päiste vahemik on esimesel lehel peidetud, kuna aruande päis sisaldab juba veergude pealkirju. Lehe päis ja jalus on teisel leheküljel peidetud, kuna see leht ei sisalda ühtegi tehingut.

    ![Genereeritud Exceli dokument töölaua rakenduses.](./media/er-paginate-excel-reports-document2.gif)

2. Kahe kande uuendamine **Intrastati** lehel, muutes **kaubanumbri** koodi **D00006** pealt **L0010** peale. Pange tähele, et uue kauba, **Aktiivs Tõstuki kõlari paari** tootenimi on pikem kui originaalkauba tootenimi, **Standardkõlar**. Selline olukord sunnib teksti vormindama loodud dokumendi vastavasse lahtrisse. Dokumendi lehekülgede saalimine ja leheküljega seotud summeerimine ja inventuur tuleb nüüd uuendada. Korrake [Intrastati deklaratsiooni kontrollaruande loomise](#generate-intrastat-control-report) jaotise samme kontrollaruande loomiseks ja ülevaatamiseks.

    Kanded esitatakse praegu kahel lehel ning lehekülje kogusummad ja kassad arvutatakse õigesti. Lehekülje päise vahemik on esimesel leheküljel õigesti peidetud ja teisel leheküljel nähtav. Lehe jalus on mõlema lehe puhul nähtav, kuna see sisaldab kandeid.

    ![Uuendatud genereeritud Exceli dokument töölaua rakenduses.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Kas on võimalik kuidagi ära tunda, millal lehe vormingu komponent töötleb viimast lehte?

**Lehekülje** komponent [ei näita](er-fillable-excel.md#page-component-limitations) teavet töödeldud lehekülje arvu ja loodud dokumendi lehtede koguarvu kohta. Sellest hoolimata saate lõpplehe äratundmiseks konfigureerida ER [valemid](er-formula-language.md). Siin on näide.

- Arvutage juba töödeldud kannete koguarv **Aruandelehe** komponendi abil. Selle arvutuse saate teha valemi `COUNT(Total.Page.Amount.Result)` abil. 
- Arvutage kannete koguarv, mida tuleb töödelda, võttes aluseks `model.CommodityRecord` **aruanderidade** komponendi jaoks konfigureeritud sidumise. Selle arvutuse saate teha valemi `COUNT(model.CommodityRecord)` abil.
- Lõpplehe äratundmiseks võrrelge kahte numbrit. Kui mõlemad väärtused on võrdsed, luuakse lõplik leht.

> [!NOTE]
> Soovitame kasutada seda lähenemist ainult siis, kui **Aruande ridade** komponendi atribuut **Lubatud** ei sisalda ühtegi valemit, mis võib käitusajal tagastada [Valesid](er-formula-supported-data-types-primitive.md#boolean) kirjeid mõnedel itereeritud [kirjetel](er-formula-supported-data-types-composite.md#record) seotud [kirjeloendis](er-formula-supported-data-types-composite.md#record-list).

## <a name="additional-resources"></a>Lisaressursid

- [Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus](er-fillable-excel.md)
- [Kasuta elektroonilise aruandluse (ER) vormingutes ANDMEKOGUMI andmeallikaid](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
