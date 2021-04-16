---
title: Exceli mallidega ER-i konfiguratsioonide taaskasutamine Wordi vormingus aruannete loomiseks
description: See teema kirjeldab, kuidas konfigureerida aruande vorminguid, mis loodi aruannete loomiseks Exceli töövihikuna, looma aruandeid Wordi dokumendina.
author: NickSelin
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 728984678d78cf626e2b30222f1d1e603e05d117
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755054"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>Exceli mallidega ER-i konfiguratsioonide taaskasutamine Wordi vormingus aruannete loomiseks

[!include [banner](../../includes/banner.md)]

Aruannete loomiseks Microsoft Wordi dokumentidena saate [konfigureerida](../er-design-configuration-word.md) uue [elektroonilise aruandluse (ER)](../general-electronic-reporting.md) [vormingu](../general-electronic-reporting.md#FormatComponentOutbound). Teise võimalusena saate taaskasutada ER-vormingut, mis oli algselt mõeldud aruannete loomiseks Exceli töövihikutena. Sellisel juhul peate asendama Exceli malli Wordi malliga.

Järgmised protseduurid näitavad, kuidas kasutaja kas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis saab konfigureerida ER-vormingut, et luua aruandeid Wordi failidena, kasutades uuesti ER-vormingut, mis loodi aruannete loomiseks Exceli failidena.

Neid toiminguid saab lõpule viia ettevõttes GBSI.

## <a name="prerequisites"></a>Eeltingimused

Nende protsesside lõpuleviimiseks peate esmalt järgima samme tegevuse juhises [Konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML](er-design-reports-openxml-2016-11.md).

Peate näidisaruande jaoks alla laadima ja kohalikult salvestama ka järgmised mallid:

- [Maksearuande mall (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=862266)
- [Maksearuande piiratud mall (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=862266)

Need protseduurid n funktsiooni jaoks, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611 (november 2016).

## <a name="select-the-existing-er-report-configuration"></a>Olemasoleva elektroonilise aruandluse aruande konfiguratsiooni valimine

1. Avage rakenduses Dynamics 365 Finance suvand **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Veenduge, et konfiguratsiooni pakkuja **Litware, Inc.** on valitud **aktiivsena**. Kui ei, järgige samme tegevuse juhises [Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks](er-configuration-provider-mark-it-active-2016-11.md).
3. Valige **Aruandluse konfiguratsioonid**. Taaskasutate olemasolevat elektroonilise aruandluse konfiguratsiooni, mis oli mõeldud aruande väljundi loomiseks OPENXML-vormingus.
4. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja valige **Töölehe aruande näide**.

    > [!NOTE]
    > Valitud ER-i vormingu mustandi versiooni saab muuta kiirkaardil **Versioonid**.

5. Valige **Kujundaja**.
6. Lehel **Vormingukujundaja** pange tähele, et juurvormingu elemendi pealkiri näitab, et praegu kasutatakse Exceli vormingut.

![Olemasoleva konfiguratsiooni valimine](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Allalaaditud Wordi malli läbivaatamine

1. Avage Wordi töölauarakenduses mailifail **SampleVendPaymDocReport.docx**, mille varem alla laadisite.
2. Kinnitage, et mall sisaldab ainult sellise dokumendi paigutust, mille soovite luua elektroonilise aruandluse väljundina.

![Wordi malli paigutus töölauarakenduses](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Exceli malli Wordi malliga asendamine ja kohandatud XML-i osa lisamine

Praegu kasutatakse Exceli dokumenti mallina väljundi loomiseks OPENXML-vormingus. Asendate selle malliWordi malli failiga SampleVendPaymDocReport.docx, mille varem alla laadisite. Lisaks laiendate Wordi malli, lisades kohandatud XML-i osa.

1. Valige rakenduses Finance lehel **Vormingukujundaja** vahekaardil **Vorming** suvand **Manused**.
2. Olemasoleva Exceli malli eemaldamiseks valige lehel **Manused** suvand **Kustuta**. Muudatuse kinnitamiseks valige **Jah**.
3. Valige **Uus** \> **Fail**.

    > [!NOTE]
    > Peate valima dokumendi tüübi, mis on ER-i parameetrites [konfigureeritud](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) talletama ER-vormingute malle.

4. Valige **Sirvi** ja seejärel sirvige ja valige fail **SampleVendPaymDocReport.docx**, mille varem alla laadisite.
5. Valige nupp **OK**.
6. Sulgege leht **Manused**.
7. Lehel **Vormingu kujundaja** väljal **Mall** sisestage või valige fail **SampleVendPaymDocReport.docx**, et kasutada seda Wordi faili Exceli malli asemel, mida kasutati varem.
8. Valige käsk **Salvesta**.

    Lisaks konfiguratsiooni muudatuste salvestamisele värskendab toiming **Salvesta** manustatud Wordi malli. Kujundatud vormingu hierarhiline struktuur lisatakse manustatud Wordi dokumenti uue kohandatud XML-i osana, mille nimeks pannakse **Aruanne**. Manustatud Wordi mall sisaldab dokumendi paigutust, mis luuakse ER-i väljundina, ja andmete struktuuri, mille ER sellesse malli käitusajal sisestab.

9. Pange tähele, et juurvormingu elemendi pealkiri näitab, et praegu kasutatakse Wordi vormingut.

    ![Exceli malli Wordi malliga asendamine ja kohandatud XML-i osa lisamine](../media/er-design-configuration-word-2016-11-image03.gif)

10. Vahekaardil **Vorming** valige **Manused**.

Saate nüüd vastendada kohandatud XML-i osa **Aruanne** elemendid Word dokumendi sisu juhtelementidega.

Kui olete tuttav protsessiga kujundada Wordi dokumendid vormidena, mis sisaldavad [sisu juhtelemente](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word), mis on vastendatud [kohandatud XML-i osade](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) elementidega, täitke dokumendi loomiseks kõik järgmise protseduuri sammud. Lisateabe saamiseks vt [Ankeetide loomine, mida kasutajad täidavad või prindivad Wordis](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Vastasel juhul jätke järgmine protseduur vahele.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Wordi dokumendi hankimine, mis sisaldab kohandatud XML-i osa ja teeb andmevastendust

1. Valige rakenduses Finance lehel **Manused** suvand **Ava**, et laadida valitud mall rakendusest Finance alla ja talletada see kohalikult Wordi dokumendina.
3. Avage Wordi töölauarakenduses äsja alla laaditud dokument.
4. Valige vahekaardil **Arendaja** suvand **XML-i vastendamise paan**.

    > [!NOTE]
    > Kui vahekaarti **Arendaja** lindil ei kuvata, kohandage linti selle lisamiseks.

5. Valige paanil **XML-i vastendamine** lehel **Kohandatud XML-i osa** kohandatud XML-i osa **Aruanne**.
6. Vastendage valitud kohandatud XML-i osa **Aruanne** elemendid ja Wordi dokumendi sisu juhtelemendid.
7. Salvestage värskendatud Wordi dokument kohalikult nimega **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Wordi malli läbivaatamine, kus kohandatud XML-i osa on vastendatud sisu juhtelementidega

1. Avage Wordi töölauarakenduses mailifail **SampleVendPaymDocReportBounded.docx**.
2. Kinnitage, et mall sisaldab sellise dokumendi paigutust, mille soovite luua elektroonilise aruandluse väljundina. Andmete kohatäidetena kasutatavad sisu juhtelemendid, mille ER sisestab selles mallis käitusajal, põhinevad vastendustel, mis on konfigureeritud kohandatud XML-i osa **Aruanne** elementide ja Wordi dokumendi sisu juhtelementide vahel.

![Wordi malli eelvaade töölauarakenduses](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Wordi malli üleslaadimine, kus kohandatud XML-i osa on vastendatud sisu juhtelementidega

1. Valige rakenduses Finance lehel **Manused** suvand **Kustuta**, et eemaldada Wordi mall, millel puuduvad vastendused kohandatud XML-i osa **Aruanne** elementide ja sisu juhtelementide vahel. Muudatuse kinnitamiseks valige **Jah**.
2. Valige **Uus** \> **Fail**, et lisada uus mallifail, mis sisaldab vastendusi kohandatud XML-i osa **Aruanne** elementide ja sisu juhtelementide vahel.

    > [!NOTE]
    > Peate valima dokumendi tüübi, mis on ER-i parameetrites [konfigureeritud](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) talletama ER-vormingute malle.

3. Valige suvand **Sirvi** ning seejärel sirvige ja valige fail **SampleVendPaymDocReportBounded.docx**, mille laadisite alla või valmistasite ette, täites protseduuri jaotises [Wordi dokumendi hankimine, mis sisaldab kohandatud XML-i osa ja teeb andmevastendust](#get-word-doc).
4. Valige nupp **OK**.
5. Sulgege leht **Manused**.
6. Valige lehel **Vormingu koostaja** väljal **Mall** dokument, mille just laadisite alla.
7. Valige käsk **Salvesta**.
8. Sulgege **Vormingu kujundaja** leht.

## <a name="mark-the-configured-format-as-runnable"></a>Konfigureeritud vormingu käivitatavaks märkimine

Redigeeritava vormingu mustandi versiooni käivitamiseks peate muutma selle [käivitatavaks](../er-quick-start2-customize-report.md#MarkFormatRunnable).

1. Valige rakenduses Finance lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** suvand **Kasutaja parameetrid**.
2. Seadke dialoogiboksis **Kasutaja parameetrid** suvandi **Käivitamissätted** väärtuseks **Jah** ja valige seejärel **OK**.
3. Vastavalt vajadusele valige **Redigeeri**, et muuta praegune leht redigeeritavaks.
4. Praegu valitud konfiguratsiooni **Töölehe aruande näide** puhul määrake suvand **Käivita mustand** valikule **Jah**.
5. Valige käsk **Salvesta**.

## <a name="run-the-format-to-create-output-in-word-format"></a>Vormingu käitamine Wordi vormingus väljundi loomiseks

1. Avage rakenduses Finance suvand **Ostureskontro** \> **Maksed** \> **Makse tööleht**.
2. Varem sisestatud makse töölehel valige suvand **Read**.
3. Valige lehel **Hankija maksed** kõik ruudustiku read.
4. Valige **Makse olek** \> **Puudub**.

    ![Hankija maksete lehel töödeldavad maksed](../media/er-design-configuration-word-2016-11-image05.png)

5. Valige toimingupaanil **Loo maksed**.
6. Ilmuvad dialoogiaknas tehke järgmist.

    1. Valige väljal **Makseviis** **Elektrooniline**.
    2. Valige väljal **Pangakonto** suvand **GBSI OPER**.
    3. Valige nupp **OK**.

7. Valige dialoogiaknas **Elektroonilise aruandluse parameetrid** suvand **OK**.
8. Loodud väljund esitatakse Wordi vormingus ja sisaldab töödeldud maksete üksikasju. Analüüsige loodud väljundit.

    ![Loodud väljund Wordi vormingus](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Lisaressursid

- [Uue ER-i konfiguratsiooni loomine Wordi vormingus aruannete loomiseks](../er-design-configuration-word.md)
- [Manustatud pildid ja kujutised ER-iga loodud dokumentides](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]