---
title: Wordi sisu juhtelementide tühistamine loodud aruannetes
description: See teema kirjeldab, kuidas konfigureerida elektroonilise aruandluse (ER) vormingut, et luua aruandeid Microsoft Word failidena, kus sisu juhtelemendid on tõkestatud.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 8c99203110cfdc7f8123c30488611d55f48e8f67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753596"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Wordi sisu juhtelementide tühistamine loodud aruannetes

[!include [banner](../includes/banner.md)]

Aruannete loomiseks Microsoft Word dokumentidena peate kujundama aruannete malli Wordi dokumendina. See mall peab sisaldama Wordi sisu juhtelemente käitusajal sisestatava teabe kohatäitjatena. Wordi vormingus aruannete Wordi dokumendi mallina kasutamiseks saate [konfigureerida](er-design-configuration-word.md) uue [elektroonilise aruandluse (ER)](general-electronic-reporting.md) [lahenduse](er-quick-start1-new-solution.md). See lahendus peab sisaldama ER-i [konfiguratsiooni](general-electronic-reporting.md#Configuration), mis sisaldab ER-i [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponenti. See ER-vorming peab olema konfigureeritud kasutama aruande loomiseks loodud malli.

Versioonis 10.0.6 ja Dynamics 365 Finance uuemates versioonides saate konfigureerida ER-vormingus valemeid, et saaks loodud dokumentides ära tõkestada Wordi sisu juhtelemente.

Järgmistes sammudes seletatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse funktsiooninõustaja rolliga kasutaja saab konfigureerida ER-vormingut, mis loob aruandeid Wordi failidena, ja summutavad mõned sisu juhtelemendid loodud aruannetes, mis on konfigureeritud Wordi malli abil.

Neid samme saab teha ettevõtte GBSI.

## <a name="prerequisites"></a>Eeltingimused

Toimingute teostamiseks tuleb esmalt läbida järgmised kolm tööjuhist:

- [OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine](./tasks/er-design-reports-openxml-2016-11.md)
- [ER-i konfiguratsioonide korduvkasutamine Exceli mallidega Wordi vormingus aruannete loomiseks](./tasks/er-design-configuration-word-2016-11.md)

Kui sooritate need ülesandejuhendite sammud, et ette valmistatakse järgmised kaubad:

- **Töölehe näidisaruande** ER-vorming, mis on konfigureeritud dokumendi loomiseks Wordi vormingus
- [Mustand](general-electronic-reporting.md#component-versioning) versioonist **näidisaruanne** ER-vormingus, mis on märgitud **käivitatavaks**
- Maksete **elektrooniline** meetod, mis on konfigureeritud kasutama hankija makse töötlemiseks **töölehe näidisaruande** ER-vormingut

Peate näidisaruande jaoks alla laadima ja kohalikult salvestama ka järgmised mallid:

- [Maksearuande 2 piiratud mall (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Allalaaditud Wordi malli läbivaatamine

1. Avage Wordi desktop rakenduses **SampleVendPaymDocReportBounded2.docx** mallifail, mille varem alla laadisite.
2. Kontrollige, et mallifail sisaldab kokkuvõtte jaotist, mis näitab maksete kogusummasid iga valuutakoodi kohta, mis on töödeldud maksetega täidetud.

    - Kokkuvõtte jaotis asub Wordi dokumendi eraldi tabelis.
    - Selle tabeli esimene rida sisaldab tabeliveergude päiseid.
    - Selle tabeli teises reas on sektsiooni üksikasjadena korduv sisu juhtelement.
    - See sisu juhtelement on vastendatud aruande **SummaryLines** välja **Aruanded** kohandatud XML-i osaga.
    - Selle vastendamise põhjal on sisu juhtelement seostatud redigeeritava **SummaryLines** ER-vormingu elemendiga.

    > [!NOTE]
    > Korduv sisu kontroll on märgistatud **SummaryLines** võtmega, mis vastab kohandatud XML-i osaväljale, millele see on vastendatud.

    ![Word malli paigutus](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Olemasoleva elektroonilise aruandluse aruande konfiguratsiooni valimine

Järgmiste sammude puhul kasutate olemasolevat ER-i konfiguratsiooni, mille konfigureerisite pärast eelnevalt mainitud ülesandejuhendite sammude lõpuleviimist.

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja valige **Töölehe aruande näide**.
4. Valige **kujundaja** valitud ER-vormingu mustandversiooni redigeerimiseks.

## <a name="replace-the-current-template-with-the-new-template"></a>Asendage olemasolev mall uue malliga

Praegu kasutatakse SampleVendPaymDocReportBounded.docx dokumenti mallina väljundi loomiseks Wordi vormingus. Järgmiste sammudena asendate selle Word malli uue Word malliga SampleVendPaymDocReportBounded2.docx, mille varem alla laadisite.

1. Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.
2. Olemasoleva Exceli malli eemaldamiseks valige lehel **Manused** suvand **Kustuta**.
3. Toimingu kinnitamiseks valige **Jah**.
4. Valige **Uus** \> **Fail**.
5. Valige **Sirvi**, ja seejärel sirvige ja valige fail **SampleVendPaymDocReportBounded2.docx** mille varem alla laadisite.
6. Valige nupp **OK**.
7. Sulgege leht **Manused**.
8. Lehel **vormingu kujundaja** väljal **mall** sisestage või valige **SampleVendPaymDocReportBounded2.docx** fail.

## <a name="run-the-format-to-create-word-output"></a>Wordi väljundi loomiseks vormingu käivitamine

1. Minge jaotisse **Ostureskontro** \> **Maksed** \> **Makse tööleht**.
2. Lehel **hankija maksed** vahekaardil **Loend**, valige kõik maksed.
3. Valige **Makse olek** \> **Puudub**.
4. Valige **Loo maksed**.
5. Valige väljal **Makseviis** **Elektrooniline**.
6. Valige väljal **Pangakonto** suvand **GBSI OPER**.
7. Valige nupp **OK**.
8. **Elektroonilise aruande** dialoogiaknas valige **Ok** ja analüüsige loodud väljundit.

    ![Hankija maksete lehel töödeldavad maksed](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Väljund esitatakse Wordi vormingus ja see sisaldab kokkuvõtte jaotist.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Redigeeritava vormingu konfigureerimine kokkuvõttejao vastu kindlustamiseks

Kui soovite loodud dokumendis oleva kokkuvõttejao eest vastu võtta, peate seda ER-vormingut käitava kasutaja taotluse alusel muutma redigeeritavat ER-vormingut.

1. Minge **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus** juurde ja avage ER-vormingu mustandversioon redigeerimiseks.
2. Valige **Aruandluse konfiguratsioonid**. 
3. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** \> **Töölehe aruande näide**.
4. Valige **Kujundaja**.
5. Laiendage **Vormingukujundaja** lehel **Word** ja valige suvand **SummaryLines**.
6. Lisage vahekaardil **Vastendamine** uus andmeallikas, et küsida kasutajalt käitusajal, kaskokkuvõtte jaotis tuleks tõkestada:

    1. Valige **Lisa juur**.
    2. Dialoogiboksis **Andmeallika lisamine** valige **Üldine\kasutaja sisendparameeter** et avada **Kasutaja sisendparameeter andmeallika parameeter** dialoogiboks.
    3. Väljale **Nimi** sisestage suvand **uiptõkesta**.
    4. Väljale **Silt** sisestage **Tõkesta kokkuvõte**.
    5. Väljal **Toimingute andmetüübi** valige või sisestage **EiJah**.
    6. Valige nupp **OK**.

7. Järgmisena tuleb rakenduse loenduse tüübile **EiJah** lisada andmeallikas, mille tüüp:

    1. Valige **Lisa juur**.
    2. Dialoogiboksis **Andmeallika lisamine** valige **Dynamics 365 for Operations\Andmeallikas** et avada **andmeallika atribuudid** dialoogiboks.
    3. Väljale **Nimi** sisestage **enumEiJah**.
    4. Väljale **Silt** sisestage **Tõkesta tingimused**.
    5. Väljal **Toimingute andmetüübi** valige või sisestage **EiJah**.
    6. Valige nupp **OK**.

8. Valitud **SummaryLinesi** vorminguelemendi puhul konfigureerige valem määramaks, millal valitud vorminguelemendiga seotud Wordi sisu juhtelement tuleb tõkestada:

    1. **Vastendamise** vahekaardil **Eemaldatud** jaotises valige **Redigeeri** et avada **[Valemikoostur](general-electronic-reporting-formula-designer.md)** lehel.
    2. **Valem** väljal, valige valem `uipSuppress = enumNoYes.Yes`.
    3. Valige **Salvesta** ja sulgege leht **Valemikoostaja**.

        > [!NOTE]
        > See valem rakendatakse loodud dokumendile pärast **kõigi teiste vorminguelementide käivitamist**. Selle valemi rakendamiseks leitakse loodud dokumendist Wordi sisu juhtelement, milleks valem on konfigureeritud (**SummaryLines** antud juhul) mis on märgistatud vorminguelemendina. Seejärel eemaldatakse see sisu juhtelement täielikult koos wordi tabeli reaga, mis seda hoiab. Kokkuvõtte jaotise üksikasjade rida eemaldatakse loodud dokumendist.
        >
        > Kujundusaja ajal võite konfigureerida vorminguelemendi jaoks valemi **Eemaldatud** kuigi teil pole wordi mallis sisu juhtelementi, mille jaoks te kasutate, silt, mis vastab vorminguelemendi nimele, mille jaoks on konfigureeritud atribuut **Eemaldatud**. Kui valideerite vormingu konstruktsiooni ajal, kuvatakse [selle vastuolu](er-components-inspections.md#i14) kohta hoiatus.
        >
        > Käitusajal ilmneb erand, kui wordi mallis, mida kasutate, puudub sisu juhtelement, mille silt vastab vorminguelemendi nimele, mille jaoks on **Eemaldatud** konfigureeritud atribuut.

    4. Vahekaardil **Vastendamine** jaotises **Eemaldatud** seadke **Emasüksusega** väärtuseks **Jah**.

        > [!NOTE]
        > Selle valiku väärtuseks tuleb määrata **jah** et eemaldada kogu Wordi tabel kokkuvõtte sektsiooni üksikasju omav rea emaobjektiks. Kui seadistate valiku väärtuseks **Ei** jääb jaotise päiserida loodud dokumenti.

9. Oma asukohakorralduse muudatuste salvestamiseks valige **Salvesta**.

    ![Loodud väljund Wordi vormingus](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Wordi väljundi loomiseks vormingu käivitamine

1. Minge jaotisse **Ostureskontro** \> **Maksed** \> **Makse tööleht**.
2. Valige loodud maksete aruanne ja valige seejärel käsk **Jooned**.
3. Valige **hankija maksete** lehel kõik read ja seejärel **makse olek** \> **Pole**.
4. Valige **Loo maksed**.
5. Valige väljal **Makseviis** **Elektrooniline**.
6. Valige väljal **Pangakonto** suvand **GBSI OPER**.
7. Valige nupp **OK**.
8. Dialoogiaknas **Elektroonilise aruande parameetrid** väljal **Kuva kokkuvõte** valige suvand **Jah**.
9. Valige **OK** ja analüüsige loodud väljundit.

    ![Loodud väljund Wordi vormingus](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Pange tähele, et väljund ei sisalda kokkuvõtte jaotist, kuna see on tõkestatud.

## <a name="additional-resources"></a>Lisaressursid

- [OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine](./tasks/er-design-reports-openxml-2016-11.md)
- [Uue ER-i konfiguratsiooni koostamine Wordi vormingus aruannete loomiseks](er-design-configuration-word.md)
- [ER-i konfiguratsioonide korduvkasutamine Exceli mallidega Wordi vormingus aruannete loomiseks](./tasks/er-design-configuration-word-2016-11.md)
- [Käitusaja probleemide ennetamiseks konfigureeritud ER-i komponendi kontrollimine](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]