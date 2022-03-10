---
title: ER-vormingu loomine Exceli vormingus manustatud piltidega lehe päistes või jalustes
description: See teema kirjeldab, kuidas kasutada elektroonilise aruandluse (ER) tööriista äridokumentide loomiseks, milles on manustatud pilte või kujusid lehe päistes või jalustes.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3f3f77a9e6104a31995c9ee398504982fe43ac9e
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323771"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>ER-vormingu loomine Exceli vormingus manustatud piltidega lehe päistes või jalustes

[!include[banner](../includes/banner.md)]

See teema selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse funktsionaalse konsultandi rolli kasutajad saavad neid ülesandeid täita.

- Parameetrite konfigureerimine [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) raamistiku jaoks.
- Importige ER [konfiguratsioonid](general-electronic-reporting.md#Configuration) mida [pakub](general-electronic-reporting.md#Provider) Microsoft ja mida kasutatakse et luua [vabas vormis arveid](../../../finance/accounts-receivable/create-free-text-invoice-new.md) mis põhinevad [mallil](er-fillable-excel.md#excel-file-component) rakenduse Microsoft Excel vormis.
- Looge [kohandatud (tuletatud)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) standardse ER-vormingu konfiguratsiooni kohandatud versioon, mida pakub Microsoft.
- Muutke kohandatud ER-vormingu konfiguratsiooni nii, et see loob vabas vormis arve aruande, milles on ettevõtte logo pilt jaluses.

Kõik selle teema ülesanded saab täita ettevõttes **USMF**. Koodi pole vaja kirjutada. Enne alustamist laadige alla ja talletage kohalikult järgmised failid.

| Kirjeldus        | Faili nimi |
|--------------------|-----------|
| Ettevõtte logo pilt | [Ettevõtte logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Sisu

- [Juriidilise isiku konfigureerimine](#ConfigureLegalEntity)
- [ER-raamistiku konfigureerimine](#ConfigureFramework)

    - [Elektroonilise aruandluse parameetrite konfigureerimine](#ConfigureParameters)
    - [ER-konfiguratsiooni pakkuja aktiveerimine](#ActivateProvider)

        - [ER-konfiguratsiooni pakkujate loendi ülevaatamine](#ReviewProvidersList)
        - [Uue ER-vormingu konfiguratsioonipakkuja lisamine](#AddProvider)
        - [Uue ER-konfiguratsiooni pakkuja aktiveerimine](#ActivateAddedProvider)

- [Standardse ER‑vormingu konfiguratsiooni importimine](#ImportERSolution1)

    - [Standardse ER-konfiguratsiooni importimine](#ImportERFormat)
    - [Imporditud ER-konfiguratsioonide ülevaatamine](#ReviewImportedERSolution)

- [Vabas vormis arve printimine standardse ER-vormingu abil](#PrintInvoice1)

    - [Seadistab prindihalduse](#ConfigurePrintManagement1)
    - [Vabas vormis arve printimine](#ProcessInvoice1)

- [Standardse ER-vormingu kohandamine](#CustomizeProvidedFormat)

    - [Kohandatud vormingu loomine](#DeriveProvidedFormat)
    - [Redigeerige kohandatud vormi](#ConfigureDerivedFormat)
    - [Kohandatud vormingu märkimine käitatavaks](#MarkFormatRunnable)

- [Vabas vormis arve printimine standardse ER-vormingu abil](#PrintInvoice2)

    - [Seadistab prindihalduse](#ConfigurePrintManagement2)
    - [Vabas vormis arve printimine](#ProcessInvoice2)

- [Lisaressursid](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Juriidilise isiku konfigureerimine

1. Avage **Organisatsiooni haldus** \> **Organisatsioonid** \> **Juriidilised isikud**.
2. Valige **Juriidilised isikud** leheküljel **Aruande ettevõtte logo pilt** kiirkaart **Muuda**.
3. Dialoogiaknas **Vali üleslaadimiseks pildifail** valige **Sirvi** ja seejärel valige **Ettevõtte logo.png** fail, mille varem laadisite.
4. Valige **Salvesta** ja sulgege leht **Mudeli vastendused**.

![Lehel Juriidilised isikud on valitud ettevõtte logo pilt.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>ER-raamistiku konfigureerimine

Elektroonilise aruandluse funktsionaalse konsultandi rolli kasutajana peate konfigureerima minimaalsete ER-parameetrite kogumi, enne kui saate hakata kasutama ER-raamistikku standardse ER-vormingu kohandatud versiooni kujundamiseks.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Elektroonilise aruandluse parameetrid**.
3. Valige lehel **Elektroonilise aruandluse parameetrid** vahekaardil **Üldine** suvandi **Luba kujundusrežiim** sätteks **Jah**.
4. Vahekaardil **Manused** määrake järgmised parameetrid.

    - Valige väljal **Konfiguratsioonid** tüüp **Fail** ettevõttele **USMF**.
    - Valige väljadel **Töö arhiiv**, **Ajutine**, **Alus** ja **Muud** tüüp **Fail**.

Lisateavet ER-parameetrite kohta vt jaotisest [ER-raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER-konfiguratsiooni pakkuja aktiveerimine

Kõigile lisatud ER-konfiguratsioonidele on märgitud omanikuks ER-konfiguratsiooni pakkuja. Sel eesmärgil kasutatakse tööruumis **Elektrooniline aruandlus** aktiveeritud ER-konfiguratsiooni pakkujat. Seega enne ER-konfiguratsioonide lisamist või redigeerimist peate aktiveerima tööruumis **Elektrooniline aruandlus** ER-konfiguratsiooni pakkuja.

> [!NOTE]
> ER-konfiguratsiooni saab redigeerida ainult konfiguratsiooni omanik. Enne ER-konfiguratsiooni redigeerimist peab olema tööruumis **Elektrooniline aruandlus** aktiveeriud vastav ER-konfiguratsiooni pakkuja.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER-konfiguratsiooni pakkujate loendi ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.
3. Lehel **Konfiguratsioonipakkuja tabel** on igal pakkuja kirjel kordumatu nimi ja URL. Vaadake üle selle lehe sisu. Kui üksuse **Litware, Inc.** (`https://www.litware.com`) kirje on juba olemas, jätke järgmine protseduur vahele [Uue ER-konfiguratsiooni pakkuja lisamine](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Uue ER-konfiguratsiooni pakkuja lisamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.
3. Lehel **Konfiguratsioonipakkujad** valige suvand **Uus**.
4. Väljale **Nimi** sisestage väärtus **Litware, Inc.**
5. Sisestage väljale **Interneti-aadress** `https://www.litware.com`.
6. Valige käsk **Salvesta**.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Uue ER-konfiguratsiooni pakkuja aktiveerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Vailge lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Litware, Inc.** ja seejärel valige **Määra aktiivne**.

Lisateabe saamiseks ER-konfiguratsiooni pakkujate kohta vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Standardse ER‑vormingu konfiguratsiooni importimine

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Standardse ER-konfiguratsiooni importimine

Oma praegusesse Microsoft Dynamics 365 Finance'i eksemplari standardsete ER-konfiguratsioonide lisamiseks peate importima need selle eksemplari jaoks konfigureeritud ER-[hoidlast](general-electronic-reporting.md#Repository).

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige **Lokaliseerimise konfiguratsioonid** lehel **Konfiguratsioonipakkujad** jaotises, valige paan **Microsoft** ja seejärel valige **Hoidla** et näha **Microsofti** hoidlate pakkujate loendit.
3. Valige lehel **Konfiguratsioonihoidlad** hoidla tüübiga **Globaalne** ja seejärel valige käsk **Ava**. Kui teilt küsitakse autoriseerimist ühenduse loomiseks [Regulatory Configuration Service'iga](../../../finance/localizations/rcs-overview.md), järgige autoriseerimise juhiseid.
4. Valige lehel **Konfiguratsioonihoidla** vasakpoolselt paanilt konfiguratsioonipuult vormingu **Vabas vormis arve (Excel)** vormi konfiguratsioon.
5. Kiirkaardil **Versioonid** valige viimane valitud ER vormingu konfiguratsiooni versioon (näiteks **240.112**) .
6. Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast alla Finance'i praegusesse eksemplari.

![Standardsete ER-konfiguratsioonide importimine lehel Konfiguratsioonihoidla.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Kui teil on probleeme [globaalsele hoidlale](er-download-configurations-global-repo.md) juurde pääsemisega, saate selle asemel [laadida konfiguratsioonid alla](download-electronic-reporting-configuration-lcs.md) Microsoft Dynamics Lifecycle Servicesist (LCS).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Imporditud ER-konfiguratsioonide ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.
3. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Arve mudel**.
4. Pange tähele, et lisaks valitud ER-vormingule **Vabas vormis arve (Excel)** imporditi teised nõutavad ER-i konfiguratsioonid. Veenduge, et konfiguratsioonipuus oleksid saadaval järgmised ER-konfiguratsioonid.

    - **Arve mudel** – see konfiguratsioon sisaldab andmemudeli ER-komponenti, mis esindab arveldamise äridomeeni andmestruktuuri.
    - **Arve mudeli vastendamine** – see konfiguratsioon sisaldab mudeli vastendamise ER-komponenti, mis kirjeldab, kuidas andmemudel käitusajal rakendusandmetega täidetakse.
    - **Vabas vormis arve (Excel)** – see konfiguratsioon sisaldab vormingu ja vormingu vastendamise ER-komponente. Vormingu komponent määrab aruande paigutuse Exceli vormingus malli põhjal. Vormingu vastenduse komponent sisaldab mudeli andmeallikat ja määratleb, kuidas seda andmeallikat kasutatakse aruande paigutuse täitmiseks käitusajal.

![Imporditud ER-konfiguratsioonid Konfiguratsioonide lehel.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Vabas vormis arve printimine standardse ER-vormingu abil

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Seadista prindihaldus

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. **Vabas vormis arve** lehel valige **FTI-00000002** arve ja seejärel valige tegevuspaani vahekaardil **Arve** **Prindihaldus** grupp, valige **Prindihaldus**.
3. Laiendage vasakul puus **prindihalduse seadistuse** lehel valikut **Moodul - müügireskontro \> Dokumendid \> Vabas vormis arve** ja seejärel **Originaal\<Default\>** üksus.
4. Valige **aruande vormingu** väljal **Vabas vormis arve (Excel)**.
5. Valige **Esc** klahv **prindihalduse seadistus** lehelt lahkumiseks ja naasmiseks **vabas vormis arve** lehele.

![Prindihalduse sätted vabas vormis arve jaoks standardses ER-vormingus prindihalduse häälestuse lehel.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Vabas vormis arve printimine

1. **Vabas vormis arve** lehel valige **FTI-00000002** arve ja seejärel valige tegevuspaani **Arve** vahekaardil **Doument** grupis, valige **Prindi** \> **Valitud**.
2. Laadige loodud arve Exceli vormingus alla ja avage see eelvaateks.
3. Pange tähele, et vastavalt Exceli malli struktuurile esitatud ER-vormingus sisaldab loodud arve lehe jalus teavet praeguse leheküljenumbri ja aruande lehtede koguarvu kohta.

![Vabas vormis loodud arve.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Standardse ER-vormingu kohandamine

Selles jaotises toodud näite puhul saate kasutada Microsofti antud ER-i konfiguratsioone, et luua Vabas vormis arve Exceli vormingus. Kuid peate lisama kohanduse, et panna ettevõtte logo pilt loodud arvete jalusesse.

Sellisel juhul peaksite Litware, Inc.-i esindajana looma (tuletama) uue ER-vormingu konfiguratsiooni, kasutades alusena Microsofti pakutavat **Vabas vormis arve (Excel)** konfiguratsiooni.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Kohandatud vormingu loomine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Arvemudel** ja seejärel valige **Vabas vormis arve (Excel)**. Litware, Inc. kasutab imporditud versiooni alusena (näiteks **240.112**) selle ER-vormingu konfiguratsiooni.
3. Rippmenüü dialoogiboksi avamiseks valige käsk **Loo konfiguratsioon**. Selle dialoogiboksi abil saate luua uue konfiguratsiooni kohandatud maksevormingu jaoks.
4. Valige väljagrupis **Uus** suvand **Tuleta nimest: Vabas vormis arve (Excel), Microsoft** valikut.
5. Valige **Nimi** väljal **Vabas vormis arve (Excel) kohandatud**.
6. Valige **Konfiguratsiooni loomine**.

![Kohandatud maksevormingu konfiguratsiooni loomine konfiguratsiooni ripploendis.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Luuakse 240.112.1 **Vabas vormis arve (Excel) kohandatud** ER-vormingu konfiguratsiooni versioonifail. Selle versiooni [olek](general-electronic-reporting.md#component-versioning) on **Mustand** ja seda saab redigeerida. Teie kohandatud ER-vormingu praegune sisu vastab Microsofti antud vormingu sisule.

![Luuakse uus versioon ER-i konfiguratsiooni versioonid konfiguratsioonide lehel.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Redigeerige kohandatud vormi

Konfigureerige oma kohandatud vorming nii, et ettevõtte logo pilt asetatakse aruande iga lehekülje jalusesse.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **Vabas vormis arve (Excel) kohandatud**.
3. Kiirkaardil **Versioonid** valige valitud konfiguratsiooni versioon **240.112.1**.
4. Valige **Kujundaja**.
5. Vorminguelementide kohta lisateabe saamiseks valige lehel **Vormingu koostaja** suvand **Kuva üksikasjad**.
6. Laiendage ja vaadake üle järgmised elemendid.

    - **Vabas vormis arve** element **Exceli** tüübis. Seda elementi kasutatakse arve loomiseks Exceli töövihiku vormingus.
    - **Vabas vormis arve \\ Arve** element **Tööleht** tüübis. Seda elementi kasutatakse loodud Exceli töövihiku töölehe loomiseks.
    - **Vabas vormis arve \\ Arve \\ Jalus** element **Jalus** tüübis. Seda elementi kasutatakse arve jaluse sisestamiseks.

7. Valige **vabas vormis arve \\ arve \\ Jalus** element.

    ![Jaluse element ER-toimingute koostajas.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Iga loodud arve lehekülje jalus sisaldab teavet praeguse leheküljenumbri ja aruande lehtede koguarvu kohta. Nagu näete, ei sisalda **Vabas vormis arve \\ Arve \\ Jalus** element tütarelemente. Seetõttu on kasutatav Exceli mall konfigureeritud kuvama saalimise üksikasju iga aruande jaluse keskel.

8. Valige **Lisa** ja seejärel valige lisatava vorminguelemendi tüüp **Excel \\ Pilt**:

    1. Väljal **Joondus** valige **Parem**.
    2. Valige **Kõrguse skaala** väljal suvand **Suhteline**.
    3. Sisestage **Skaala protsendina** **70**.
    4. Valige nupp **OK**.

        > [!NOTE]
        > **Exceli \\ Pilt** elementi kasutatakse ettevõtte logo pildi lisamiseks ja selle joondamiseks lehe jaluse paremal küljel.

    ![Komponendi atribuutide dialoogiboksis pildi elemendi atribuudid.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Valige vasakult vormingustruktuuri puult äsja lisatud **Pildi** element ja seejärel laiendage vahekaardil **Vastendamine** **mudeli** andmeallikat.
10. Laienda **mudel.makse** \> **mudel.ArveBaas \> model.ArveBaas.EttevõtteInfo** ja seejärel valige **mudel.ArveBaas.EttevõtteInfo.Logo** andmeallika väli. Andmeallika väli [Konteiner](er-formula-supported-data-types-composite.md#container) näitab ettevõtte logopilti meediumisisuna.
11. Valige **Seo**. **Pildi** vormingu element on nüüd seotud andmeallika **mudel.ArveBaasEttevõtteInfo.Logo** andmeallika väljaga. Seepärast pannakse käitusajal ettevõtte logo pilt loodud arvete jalusesse.

    ![Pildi vormingu element on nüüd seotud andmeallika model.InvoiceBase.CompanyInfo.Logo andmeallika väljaga ER operatsioonikujundajas.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Valige käsk **Salvesta** ja sulgege leht **Kujundaja**.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Kohandatud vormingu märkimine käitatavaks

Kuna teie kohandatud vormingu esimene versioon on loodud ja selle olek on **Mustand**, saate selle vormingu käitada testimise eesmärgil. Aruande käitamiseks peate töötlema hankija makset makseviisi abil, mis viitab teie kohandatud ER-vormingule. Kui toote rakendusest ER-vormingu võetakse vaikimisi [arvesse](general-electronic-reporting.md#component-versioning) ainult versioone, mille olek on **Lõpule viidud** või **Ühiskasutusse antud**. Selle käitumise abil saab vältida ER-vormingute kasutamist, mille koostamine on lõpetamata. Kuid oma testikäivitustel saate sundida rakendust kasutama teie ER-vormingu versiooni, mille olekuks on **Mustand**. Sedasi saate korrigeerida praeguse vormingu versiooni, kui muudatusi on vaja. Lisateavet vt jaotisest [Kohaldatavus](electronic-reporting-destinations.md#applicability).

ER-vormingu mustandversiooni kasutamiseks peate ER-vormingu selgelt märgistama.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Seadke dialoogiboksis **Kasutaja parameetrid** suvandi **Käivitamissätted** väärtuseks **Jah** ja valige seejärel **OK**.
4. Valige **Redigeeri** et muuta olemasolev leht redigeeritavaks, konfiguratsioonipuul vasakpoolsel paanil valige **Vabas vormis arve (Excel) kohandatud**.
5. Seadke suvandi **Käivita mustand** väärtuseks **Jah**.

![Kohandatud vormingu märkimine konfiguratsioonide lehel käivitatavaks.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Vabas vormis arve printimine standardse ER-vormingu abil

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Seadista prindihaldus

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. **Vabas vormis arve** lehel valige **FTI-00000002** arve ja seejärel valige tegevuspaani vahekaardil **Arve** **Prindihaldus** grupp, valige **Prindihaldus**.
3. Laiendage vasakul puus **prindihalduse seadistuse** lehel valikut **Moodul - müügireskontro** \> **Dokumendid** \> **Vabas vormis arve** ja seejärel valige **Originaal** **\<Default\>** üksus.
4. Valige **aruande vormingu** väljal **Vabas vormis arve (Excel) kohandatud**.
5. Valige **Esc** klahv **prindihalduse seadistus** lehelt lahkumiseks ja naasmiseks **vabas vormis arve** lehele.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Vabas vormis arve printimine

1. **Vabas vormis arve** lehel valige **FTI-00000002** arve ja seejärel valige tegevuspaani **Arve** vahekaardil **Doument** grupis, valige **Prindi** \> **Valitud**.
2. Laadige loodud arve Exceli vormingus alla ja avage see eelvaateks.
3. Pange tähele, et vastavalt kohandatud ER-vormingu struktuurile sisaldab loodud arve lehe jalus lisaks aruande saalimise teabele ettevõtte logo pilti.

![Loodud vabas vormis arve ettevõtte logopildiga lehe jaluses.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Lisaressursid

- [Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus](er-fillable-excel.md)
- [Manustatud pildid ja kujutised ER-iga loodud dokumentides](electronic-reporting-embed-images-shapes.md)
