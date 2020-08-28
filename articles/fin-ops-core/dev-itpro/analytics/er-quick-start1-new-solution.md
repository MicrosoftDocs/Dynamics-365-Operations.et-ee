---
title: Uue ER-i lahenduse kujundamine kohandatud aruande printimiseks
description: Selles teemas selgitatakse, kuidas kujundada elektroonilise aruandluse (ER) lahendust kohandatud aruande printimiseks.
author: NickSelin
manager: AnnBe
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ede88bc1767304a86a86ec27365db9403c5a951d
ms.sourcegitcommit: 4909e55529f03310d24b7e40d52751e24d35259b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3678244"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Uue ER-i lahenduse kujundamine kohandatud aruande printimiseks

[!include[banner](../includes/banner.md)]

Järgmistes etappides on seletatud, kuidas süsteemiadministraatori, elektroonilise aruandluse arendaja või elektroonilise aruandluse funktsionaalse konsultandi rolli omav kasutaja saab konfigureerida ER-i raamistiku parameetreid, kujundada uue ER-i lahenduse jaoks vajalikke ER-i konfiguratsioone, et pääseda juurde konkreetse äridomeeni andmetele ja luua kohandatud aruannet Microsoft Office'i vormingus. Neid toiminguid saab teha ettevõttes **USMF**.

- [ER-raamistiku konfigureerimine](#ConfigureFramework)

    - [Elektroonilise aruandluse parameetrite konfigureerimine](#ConfigureParameters)
    - [ER-konfiguratsiooni pakkuja aktiveerimine](#ActivateProvider)

        - [ER-konfiguratsiooni pakkujate loendi ülevaatamine](#ReviewProvidersList)
        - [Uue ER-vormingu konfiguratsioonipakkuja lisamine](#AddProvider)
        - [ER-konfiguratsiooni pakkuja aktiveerimine](#ActivateAddedProvider)

- [Domeenipõhise andmemudeli kujundamine](#DesignModel)

    - [Uue andmemudeli konfiguratsiooni importimine](#ImportDataModel)
    - [Uue andmemudeli konfiguratsiooni loomine](#DesignDataModel)

        - [Andmemudelile nime panemine](#NameDataModel)
        - [Andmemudeli väljade lisamine](#FieldsEntry)
        - [Andmemudeli kujunduse lõpuleviimine](#CompleteDataModel)

- [Mudelivastenduse kujundamine konfigureeritud andmemudelile](#DesignMapping)

    - [Uue mudelivastenduse konfiguratsiooni importimine](#ImportModelMapping)
    - [Uue mudelivastenduse konfiguratsiooni loomine](#CreateModelMapping)

        - [Uue mudelivastenduse komponendi kujundamine](#DesignMappingComponent)
        - [Andmeallikate lisamine rakenduse tabelitele juurdepääsemiseks](#AddMmDataSource1)
        - [Andmeallikate lisamine rakenduse loeteludele juurdepääsemiseks](#AddMmDataSource2)
        - [ER-i siltide lisamine aruande loomiseks määratud keeles](#AddMmLabels)
        - [Andmeallika lisamine loetelu väärtuste võrdlemise tulemuste muutmiseks tekstiväärtuseks](#AddMmDataSource3)
        - [Andmeallikate sidumine andmemudeli väljadega](#AddMmBindings1)
        - [Mudelivastenduse kujunduse lõpuleviimine](#CompleteModelMapping)

- [Kohandatud aruande malli kujundamine](#DesignReportTemplate)
- [Vormingu kujundamine](#DesignFormat)

    - [Kujundatud vormingu konfiguratsiooni importimine](#FormatImport)
    - [Uue vormingu konfiguratsiooni loomine](#FormatCreate)

        - [Aruandemalli importimine](#ImportReportTemplate)
        - [Vormingu konfigureerimine](#ConfigureFormat)
        - [Andmesidumise määratlemine aruande pealkirja jaoks](#DefineFormatBindings)
        - [Mudeli andmeallika ülevaatamine](#ReviewModelDataSource)
        - [Vorminguelementide sidumine andmeallika väljadega](#BindFormatElements)

    - [Kujundatud vormingu käivitamine ER-is](#RunFormatFromER)

- [Kujundatud vormingu häälestamine](#TuneFormat)

    - [Vormingu muutmine loodud dokumendi nime muutmiseks](#ModifyToChangeName)
    - [Vormingu muutmine küsimuste järjekorra muutmiseks](#ModifyToOrder)
    - [Muudetud vormingu käivitamine ER-is](#RunFormatFromER2)
    - [Vormingu kujunduse lõpuleviimine](#CompleteFormat)

- [Rakenduse artefaktide arendamine kujundatud aruande kutsumiseks](#DevelopCustomCode)

    - [Lähtekoodi muutmine](#ModifySourceCode)

        - [Andmelepingu klassi lisamine](#DataContractClass)
        - [UI-koostaja klassi lisamine](#UIBuilderClass)
        - [Andmepakkuja klassi lisamine](#DataProviderClass)
        - [Siltide faili lisamine](#LabelsFile)
        - [Aruandeteenuse klassi lisamine](#ServiceClass)
        - [Aruandekontrolleri klassi lisamine](#ControllerClass)
        - [Menüüelemendi lisamine](#MenuItem)
        - [Menüüelemendi lisamine menüüle](#Menu)
        - [Visual Studio projekti koostamine](#BuildVSProject)

    - [Vormingu käivitamine rakenduses](#RunFormatFromApp)

- [Kujundatud ER-i lahenduse häälestamine](#TuneSolution)

    - [Mudelivastenduse muutmine](#ModifyModelMapping)

        - [Andmeallikate lisamine andmelepingu objektile juurdepääsemiseks](#AddDataSource1)
        - [Andmeallika lisamine ER-i vorminguvastenduse kirjetele juurdepääsemiseks](#AddDataSource2)
        - [Andmeallika lisamine töötava ER-i vorminguvastenduse kirjele juurdepääsemiseks](#AddDataSource3)
        - [Töötava ER-i vormingu nime sisestamine andmemudelisse](#AddBinding)
        - [Mudelivastenduse kujunduse lõpuleviimine](#CompleteModelMapping2)

    - [Vormingu muutmine](#ModifyFormat)

        - [Uue vorminguelemendi lisamine](#AddFormatElement)
        - [Lisatud vorminguelemendi sidumine](#BindAddedFormatElement)
        - [Vormingu kujunduse lõpuleviimine](#CompleteFormat2)

    - [Vormingu käivitamine rakenduses](#RunFormatFromApp2)
    - [Vormingu käivitamine ER-is](#RunFormatFromER3)
    - [Vormingu sihtkoha konfigureerimine ekraanil eelvaatamiseks](#ConfigureDestination)
    - [Vormingu käivitamine rakenduses selle eelvaatamiseks PDF-dokumendina](#RunFormatFromApp3)

- [Lisaressursid](#References)

Selles näites loote uue ER-i lahenduse mooduli [Küsimustik](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) jaoks. See uus ER-i lahendus võimaldab teil kujundada aruande, kasutades Microsoft Exceli töölehte mallina. Seejärel saate lisaks olemasoleva SQL Serveri aruandlusteenuste (SSRS) aruande loomisele luua aruande **Küsimustik** Excelis või PDF-vormingus. Vajaduse korral saate uut aruannet ka hiljem muuta. Koodi pole vaja kirjutada.

1. Olemasoleva aruande käivitamiseks avage **Küsimustik** \> **Kujundus** \> **Küsimustike aruanne**.

    ![Küsimustike aruande menüüelemendi valimine küsimustiku moodulis, et käivitada olemasolev SSRS-aruanne](./media/er-quick-start1-application-menu-origin.png)

2. Määrake dialoogiboksis **Küsimustike aruanne** valikukriteeriumid. Lisage filter, et aruanne sisaldaks ainult küsimustikku **SBCCrsExam**.

    ![Valikukriteeriumide täpsustamine küsimustike aruande dialoogiboksis](./media/er-quick-start1-ssrs-report-dialog.png)

Järgmisel illustratsioonil on kujutatud SSRS-i aruande loodud versioon küsimustiku **SBCCrsExam** jaoks.

![Loodud SSRS-aruanne](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>ER-raamistiku konfigureerimine

Elektroonilise aruandluse arendaja rollis kasutajana peate konfigureerima minimaalse ER-i parameetrite kogumi, enne kui saate hakata kasutama ER-i raamistikku oma uue ER-i lahenduse kujundamiseks.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine

1. Avage **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige tööruumis **Elektrooniline aruandlus** suvand **Elektroonilise aruandluse parameetrid**.
3. Seadke lehel **Elektroonilise aruandluse parameetrid** vahekaardil **Üldine** suvandi **Luba kujundusrežiim** väärtuseks **Jah**.
4. Määrake vahekaardil **Manused** järgmised parameetrid.

    - Seadke välja **Konfiguratsioonid** väärtuseks **Fail** ettevõtte **USMF** jaoks.
    - Seadke väljade **Tööarhiiv**, **Ajutine**, **Alus** ja **Muud** väärtuseks **Fail**.

Lisateavet ER-parameetrite kohta vt jaotisest [ER-raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>ER-konfiguratsiooni pakkuja aktiveerimine

Kõigi ER-i konfiguratsioonide omanikuks on märgitud ER-i konfiguratsiooni pakkuja. Seega peate enne ER-i konfiguratsioonide lisamist või redigeerimist aktiveerima tööruumis **Elektrooniline aruandlus** ER-i konfiguratsiooni pakkuja.

> [!NOTE]
> ER-konfiguratsiooni saab redigeerida ainult selle omanik. Seega enne ER-konfiguratsiooni redigeerimist pea olema tööruumis **Elektrooniline aruandlus** aktiveeriud vastav ER-konfiguratsiooni pakkuja.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>ER-konfiguratsiooni pakkujate loendi ülevaatamine

1. Avage **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** suvand **Konfiguratsioonipakkujad**.
3. Lehel **Konfiguratsioonipakkujad** on igal konfiguratsioonipakkuja kirjel kordumatu nimi ja URL. Vaadake üle selle lehe sisu. Kui üksuse **Litware, Inc.** (`https://www.litware.com`) kirje on juba olemas, jätke järgmine protseduur vahele [Uue ER-konfiguratsiooni pakkuja lisamine](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Uue ER-konfiguratsiooni pakkuja lisamine

1. Lehel **Konfiguratsioonipakkujad** valige suvand **Uus**.
2. Sisestage väljale **Nimi** väärtus  **Litware, Inc.**
3. Sisestage väljale **Interneti-aadress**  `https://www.litware.com`.
4. Valige **Salvesta**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>ER-konfiguratsiooni pakkuja aktiveerimine

1. Avage **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige tööruumis **Elektrooniline aruandlus** konfiguratsioonipakkuja **Litware, Inc.**
3. Valige **Määra aktiivseks**.

Lisateabe saamiseks ER-konfiguratsiooni pakkujate kohta vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Domeenipõhise andmemudeli kujundamine

Peate looma uue ER-i konfiguratsiooni, mis sisaldab [andmemudeli](general-electronic-reporting.md#data-model-and-model-mapping-components) komponenti **Küsimustiku** äridomeeni jaoks. Seda andmemudelit kasutatakse hiljem andmeallikana, kui kujundate ER-i vormingut aruande **Küsimustik** loomiseks.

Kui täidate jaotises [Uue andmemudeli konfiguratsiooni importimine](#ImportDataModel) toodud juhised, saate vajaliku andmemudeli importida esitatud XML-failist. Teise võimalusena saate täita jaotise [Uue andmemudeli konfiguratsiooni loomine](#DesignDataModel) juhised, et kujundada see andmemudel täiesti algusest.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Uue andmemudeli konfiguratsiooni importimine

1. Laadige alla fail [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) ja salvestage see oma kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.
5. Valige **Sirvi** ning seejärel otsige üles ja valige fail **Questionnaires model.version.1.xml**.
6. Konfiguratsiooni importimiseks valige **OK**.

Jätkamiseks jätke järgmine protseduur [Uue andmemudeli konfiguratsiooni loomine](#DesignDataModel) vahele.

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Uue andmemudeli konfiguratsiooni loomine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
3. Valige **Konfiguratsiooni loomine**.
4. Sisestage rippdialoogiboksi väljale **Nimi** tekst **Küsimustiku mudel**.
5. Konfiguratsiooni loomiseks valige **Loo konfiguratsioon**.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Andmemudelile nime panemine

1. Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku mudel**.
2. Valige **Kujundaja**.
3. Sisestage lehe **Andmemudeli kujundaja** kiirkaardi **Üldine** väljale **Nimi** tekst <a name="DataModeName"></a>**Questionnaires**.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Uute andmemudeli väljade lisamine

1. Valige lehel **Andmemudeli kujundaja** suvand **Uus**.
2. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Valige uue sõlme tüübiks **Mudeli juur**.
    2. Sisestage väljale **Nimi** tekst <a name="RootDefinitionName"></a>**Root**.
    3. Uue sõlme lisamiseks valige **Lisa**.

    Seda juuredeskriptorit kasutatakse aruande **Küsimustik** jaoks andmete esitamiseks. Ühel andmemudelil võib olla mitu deskriptorit. Igat deskriptorit saab määrata ühe ER-i vormingu jaoks, et tuvastada aruande loomiseks vajalikud andmed.

3. Valige uuesti **Uus** ja seejärel järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Valige uue sõlme tüübiks **Aktiivse sõlme tütar**.
    2. Sisestage väljale **Nimi** tekst **CompanyName**.
    3. Valige väljalt **Üksuse tüüp** suvand **String**.
    4. Uue välja lisamiseks valige **Lisa**.

    Seda välja on vaja, et edastada praeguse ettevõtte nimi ER-i aruandesse, mis kasutab seda andmemudelit andmeallikana.

4. Valige uuesti **Uus** ja seejärel järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Valige uue sõlme tüübiks **Aktiivse sõlme tütar**.
    2. Sisestage väljale **Nimi** tekst **Questionnaire**.
    3. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
    4. Uue välja lisamiseks valige **Lisa**.

    Seda välja kasutatakse selleks, et edastada küsimustike loend ER-i aruandesse, mis kasutab seda andmemudelit andmeallikana.

5. Valige sõlm **Küsimustik**.
6. Jätkake samal viisil vajalike väljade lisamist redigeeritavasse andmemudelisse, kuni olete lõpetanud järgmise andmemudeli struktuuri.

    | Välja tee                                                    | Andmetüüp   | Välja kirjeldus / tagastatav väärtus |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Juur                                                          |             | Viitepunkt küsimustiku andmete taotlemiseks. |
    | Root\\CompanyName                                             | String      | Praeguse ettevõtte nimi. |
    | Root\\ExecutionContext                                        | Salvestamine      | Vormingu käivitamise üksikasjad. |
    | Root\\ExecutionContext\\FormatName                            | String      | Käivitatud ER-i vormingu nimi. |
    | Root\\Questionnaire                                           | Kirjete loend | Küsimustike loend |
    | Root\\Questionnaire\\Active                                   | String      | Praeguse küsimustiku olek. |
    | Root\\Questionnaire\\Code                                     | String      | Praeguse küsimustiku kood. |
    | Root\\Questionnaire\\Description                              | String      | Praeguse küsimustiku kirjeldus. |
    | Root\\Questionnaire\\QuestionnaireType                        | String      | Praeguse küsimustiku tüüp. |
    | Root\\Questionnaire\\QuestionOrder                            | String      | Praeguse küsimustiku numbriline järjekord. |
    | Root\\Questionnaire\\ResultsGroup                             | Salvestamine      | Praeguse küsimustiku tulemuste parameetrid. |
    | Root\\Questionnaire\\ResultsGroup\\Code                       | String      | Praeguse tulemusegrupi identifitseerimiskood. |
    | Root\\Questionnaire\\ResultsGroup\\Description                | String      | Praeguse tulemusegrupi kirjeldus. |
    | Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Tegelik        | Maksimaalne punktide arv, mida on võimalik saada. |
    | Root\\Questionnaire\\Question                                 | Kirjete loend | Praeguse küsimustiku küsimuste loend. |
    | Root\\Questionnaire\\Question\\CollectionSequenceNumber       | Täisarv     | Praeguse vastuste kogumi järjekorranumber. |
    | Root\\Questionnaire\\Question\\Id                             | String      | Praeguse küsimuse identifitseerimiskood. |
    | Root\\Questionnaire\\Question\\MustBeCompleted                | String      | Lipp, mis näitab, kas praegusele küsimusele tuleb vastata. |
    | Root\\Questionnaire\\Question\\PrimaryQuestion                | String      | Lipp, mis näitab, kas praegune küsimus on esmane. |
    | Root\\Questionnaire\\Question\\SequenceNumber                 | Täisarv     | Praeguse küsimuse järjekorranumber. |
    | Root\\Questionnaire\\Question\\Text                           | String      | Praeguse küsimuse tekst. |
    | Root\\Questionnaire\\Question\\Answer                         | Kirjete loend | Praeguse küsimuse vastuste loend. |
    | Root\\Questionnaire\\Question\\Answer\\CorrectAnswer          | String      | Lipp, mis näitab, kas praegune vastus on õige. |
    | Root\\Questionnaire\\Question\\Answer\\Points                 | Tegelik        | Punktid, mis saadakse praeguse vastuse valimisel. |
    | Root\\Questionnaire\\Question\\Answer\\SequenceNumber         | Täisarv     | Praeguse vastuse järjekorranumber. |
    | Root\\Questionnaire\\Question\\Answer\\Text                   | String      | Praeguse vastuse tekst. |

    Järgmisel illustratsioonil on kujutatud lõpule viidud redigeeritav andmemudel lehel **Andmemudeli kujundaja**.

    ![Konfigureeritud andmemudel ER-i andmemudeli kujundajas](./media/er-quick-start1-model2.png)

7. Salvestage muudatused.
8. Sulgege leht **Andmemudeli kujundaja**.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Andmemudeli kujunduse lõpuleviimine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku mudel**.
3. Valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.
4. Valige **Muuda olekut** \> **Lõpule viidud**.

Selle konfiguratsiooni versiooni 1 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**. Versiooni 1 ei saa enam muuta. See versioon sisaldab konfigureeritud andmemudelit ja seda saab kasutada teiste ER-i konfiguratsioonide alusena. Luuakse selle konfiguratsiooni versioon 2, mille olek on **Mustand**. Saate seda versiooni redigeerida, et kohandada andmemudelit **Küsimustik**.

![Redigeeritava ER-i konfiguratsiooni versioonid lehel „Konfiguratsioonid”](./media/er-quick-start1-model-configuration.png)

Lisateavet ER-i konfiguratsioonide versioonide kohta leiate teemast [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Konfigureeritud andmemudel esindab abstraktselt äridomeeni **Küsimustik** ega ole seotud artefaktidega, mis kuuluvad rakendusse Microsoft Dynamics 365 Finance.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Mudelivastenduse kujundamine konfigureeritud andmemudelile

Elektroonilise aruandluse arendaja rollis kasutajana peate looma uue ER-i konfiguratsiooni, mis sisaldab [mudelivastenduse](general-electronic-reporting.md#data-model-and-model-mapping-components) komponenti andmemudeli **Küsimustik** jaoks. Kuna see komponent kasutab Finance'i jaoks mõeldud konfigureeritud andmemudelit, on see rakenduse Finance põhine. Peate konfigureerima mudelivastenduse komponendi, et määrata rakenduse objektid, mida tuleb käitusajal kasutada rakenduse andmete lisamiseks konfigureeritud andmemudelisse. Selle ülesande lõpetamiseks peate teadma Finance'is oleva äridomeeni **Küsimustik** andmestruktuuri juurutamise üksikasju.

Kui täidate järgnevas jaotises [Uue mudelivastenduse konfiguratsiooni importimine](#ImportModelMapping) toodud juhised, saate vajaliku mudelivastenduse konfiguratsiooni importida esitatud XML-failist. Teise võimalusena saate täita jaotise [Uue mudelivastenduse konfiguratsiooni loomine](#CreateModelMapping) juhised, et kujundada see mudelivastendus täiesti algusest.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Uue mudelivastenduse konfiguratsiooni importimine

1. Laadige alla fail [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) ja salvestage see oma kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.
5. Valige **Sirvi** ning seejärel otsige üles ja valige fail **Questionnaires mapping.version.1.1.xml**.
6. Konfiguratsiooni importimiseks valige **OK**.

Jätkamiseks jätke järgmine protseduur [Uue mudelivastenduse konfiguratsiooni loomine](#CreateModelMapping) vahele.

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Uue mudelivastenduse konfiguratsiooni loomine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku mudel**.
3. Valige **Konfiguratsiooni loomine**.
4. Dialoogiakna ripploendis järgige allolevaid etappe.

    1. Valige väljal **Uus** suvand **Küsimustike andmemudelil põhinev mudelivastendus**.
    2. Sisestage väljale **Nimi** tekst **Küsimustiku vastendamine**.
    3. Valige väljal **Andmemudeli definitsioon** definitsioon **Juur**.
    4. Konfiguratsiooni loomiseks valige **Loo konfiguratsioon**.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Uue mudelivastenduse komponendi kujundamine

1. Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku vastendamine**.
2. Valige **Kujundaja**, et avada vastenduste loend.
3. Valige vastendus **Küsimustike vastendamine**, mis lisati automaatselt definitsiooni **Juur** jaoks
4. Valige **Kujundaja**, et alustada valitud vastenduse konfigureerimist.

Definitsiooni **Juur** jaoks lisatakse automaatselt uus vastendus. Sellel vastendusel suund **Mudelisse**. Seetõttu saab seda vastendust kasutada selleks, et lisada vajalikud andmed andmemudelisse.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Andmeallikate lisamine rakenduse tabelitele juurdepääsemiseks

Peate konfigureerima andmeallikad, et pääseda juurde küsimustiku üksikasju sisaldavatele rakenduse tabelitele.

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.
2. Lisage uus andmeallikas, mida kasutatakse tabelile KMCollection juurdepääsemiseks, kus iga kirje tähistab ühte küsimustikku.

    1. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    2. Sisestage dialoogiboksis väljale **Nimi** väärtus **Questionnaire**.
    3. Sisestage väljale **Tabel** väärtus **KMCollection**.
    4. Määrake suvandi **Küsi päringut** väärtuseks **Jah**. Seejärel saate selle tabeli jaoks määrata [filtreerimissuvandid](../../fin-ops/get-started/advanced-filtering-query-options.md), mida rakendatakse käitusajal süsteemipäringu dialoogiboksis.
    5. Uue andmeallika lisamiseks valige **OK**.

3. Valige paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.
4. Lisage uus andmeallikas, mida kasutatakse tabelile KMQuestion juurdepääsemiseks, kus iga kirje tähistab ühte küsimust küsimustikus.

    1. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    2. Sisestage dialoogiboksis väljale **Nimi** väärtus **Question**.
    3. Sisestage väljale **Tabel** väärtus **KMQuestion**.
    4. Uue andmeallika lisamiseks valige **OK**.

5. Valige paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.
6. Lisage uus andmeallikas, mida kasutatakse tabelile KMAnswer juurdepääsemiseks, kus iga kirje tähistab ühte vastust küsimustikus olevale küsimusele.

    1. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    2. Väljale **Nimi** sisestage **Answer**.
    3. Sisestage väljale **Tabel** väärtus **KMAnswer**.
    4. Uue andmeallika lisamiseks valige **OK**.

7. Valige paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.
8. Lisage uus arvutatud väli, mida kasutatakse selleks, et pääseda ematabeli KMCollection kõikide kirjete kaudu juurde tabeli KMQuestionResultGroup kirjetele.

    1. Valige paanil **Andmeallikad** suvand **Küsimustik**.
    2. Valige **Lisa**.
    3. Sisestage dialoogiboksis väljale **Nimi** väärtus **\$ResultGroup**.
    4. Valige **Valemi redigeerimine**.
    5. Sisestage [ER-i valemiredaktoris](general-electronic-reporting-formula-designer.md) väljale **Valem** väärtus **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)**, et kasutada tabelite KMCollection ja KMQuestionResultGroup vahelise üks-mitmele seose [teed](er-formula-language.md#paths).
    6. Valige **Salvesta** ja sulgege seejärel valemiredaktor.
    7. Uue arvutatud välja lisamiseks valige **OK**.

9. Valige paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.
10. Lisage uus arvutatud väli, mida kasutatakse selleks, et pääseda ematabeli KMCollectionQuestion kõikide kirjete kaudu juurde tabeli KMQuestion küsimusekirjetele.

    1. Valige paanil **Andmeallikad** suvand **Küsimustik**.
    2. Laiendage sõlme **\<Seosed**, mis sisaldab tabeli KMCollection üks-mitmele seoseid.
    3. Valige seotud tabel **KMCollectionQuestion** ja seejärel **Lisa**.
    4. Sisestage dialoogiboksis väljale **Nimi** väärtus **\$Question**.
    5. Valige **Valemi redigeerimine**.
    6. Sisestage valemiredaktoris väljale **Valem** väärtus **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))**, et tagastada asjakohased küsimusekirjed tabelist KMQuestion.
    7. Valige **Salvesta** ja sulgege seejärel valemiredaktor.
    8. Uue arvutatud välja lisamiseks valige **OK**.

11. Valige paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.
12. Lisage uus arvutatud väli, mida kasutatakse selleks, et pääseda ematabeli KMQuestion kõikide kirjete kaudu juurde tabeli KMAnswer vastusekirjetele.

    1. Valige paanil **Andmeallikad** suvand **Questionnaire.\<Relations.KMCollectionQuestion.\$Question** ja seejärel valige **Lisa**.
    2. Sisestage dialoogiboksis väljale **Nimi** väärtus **\$Answer**.
    3. Valige **Valemi redigeerimine**.
    4. Sisestage valemiredaktoris väljale **Valem** väärtus **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)**, et tagastada asjakohased vastusekirjed tabelist KMAnswer.
    5. Valige **Salvesta** ja sulgege seejärel valemiredaktor.
    6. Uue arvutatud välja lisamiseks valige **OK**.

13. Valige paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabel**.
14. Lisage uus andmeallikas, mida kasutatakse tabeli CompanyInfo meetoditele juurdepääsemiseks. Pange tähele, et selle tabeli meetod **find()** tagastab kirje, mis tähistab Finance'i praeguse eksemplari ettevõtet, mille jaoks seda vastendust kutsutakse.

    1. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    2. Sisestage dialoogiboksis väljale **Nimi** väärtus **CompanyInfo**.
    3. Sisestage väljale **Tabel** väärtus **CompanyInfo**.
    4. Uue andmeallika lisamiseks valige **OK**.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Andmeallikate lisamine rakenduse loeteludele juurdepääsemiseks

Peate konfigureerima andmeallikad, et pääseda rakenduse loeteludele juurde ja võrrelda nende väärtusi rakenduse tabelites olevate väljade väärtustega, mille tüüp on **Loetelu**. Peate kasutama võrdluse tulemust andmemudeli asjakohaste väljade täitmiseks.

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Loetelu**.
2. Lisage uus andmeallikas, mida kasutatakse loetelu **EnumAppNoYes** väärtustele juurdepääsemiseks.

    1. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    2. Sisestage dialoogiboksis väljale **Nimi** väärtus **EnumAppNoYes**.
    3. Sisestage väljale **Loetelu** väärtus **NoYes**.
    4. Uue andmeallika lisamiseks valige **OK**.

3. Valige paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Loetelu**.
4. Lisage uus andmeallikas, mida kasutatakse loetelu **KMCollectionQuestionMode** väärtustele juurdepääsemiseks.

    1. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    2. Sisestage dialoogiboksis väljale **Nimi** väärtus **EnumAppQuestionOrder**.
    3. Sisestage väljale **Loetelu** väärtus **KMCollectionQuestionMode**.
    4. Uue andmeallika lisamiseks valige **OK**.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>ER-i siltide lisamine aruande loomiseks määratud keeles

Saate lisada ER-i silte, et konfigureerida mõned oma andmeallikad tagastama väärtusi, mis sõltuvad mudelivastenduse kutse kontekstis määratletud keelest.

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallikad** suvand **Vastus** ja seejärel **Redigeeri**.
2. Aktiveerige väli **Silt**.
3. Valige käsk **Tõlgi**.
4. Järgige dialoogiboksis **Teksti tõlkimine** allolevaid etappe.

    1. Sisestage väljale **Sildi ID** väärtus **PositiveAnswer**.
    2. Sisestage väljale **Tekst vaikekeeles** väärtus **Yes**.
    3. Valige käsk **Tõlgi**.
    4. Sisestage väljale **Sildi ID** väärtus **NegativeAnswer**.
    5. Sisestage väljale **Tekst vaikekeeles** väärtus **No**.
    6. Valige käsk **Tõlgi**.

5. Sulgege dialoogiboks **Teksti tõlkimine**.
6. Valige **Tühista**.

![ER-i siltide lisamine redigeeritavale mudelivastendusele](./media/er-quick-start1-adding-labels.png)

Sisestasite ER-i sildid ainult vaikekeele jaoks. Lisateavet selle kohta, kuidas ER-i silte saab teistesse keeltesse tõlkida, leiate teemast [Mitmekeelsete aruannete kujundamine](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Andmeallika lisamine loetelu väärtuste võrdlemise tulemuste muutmiseks tekstiväärtuseks

Kuna peate võrdlemise tulemused eri allikate jaoks mitu korda loetelu väärtuste ja teksti väärtuste vahel teisendama, on hea mõte konfigureerida see loogika ühe andmeallikana. Selle andmeallika korduvkasutatavaks muutmiseks peate selle konfigureerima parameetritega andmeallikana. Lisateavet leiate teemast [Arvutatud välja tüüpi ER-i andmeallikate parameetritega kutsete toetamine](er-calculated-field-type.md).

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Üldine\\Tühi konteiner**.
2. Lisage uus konteineri tüüpi andmeallikas.

    1. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    2. Sisestage dialoogiboksis väljale **Nimi** väärtus **Helper**.
    3. Uue konteineri tüüpi andmeallika lisamiseks valige **OK**.

3. Valige paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.
4. Lisage uus andmeallikas.

    1. Valige paanil **Andmeallikad** suvand **Abiline**.
    2. Valige **Lisa**.
    3. Sisestage rippdialoogiboksis väljale **Nimi** väärtus **NoYesEnumToString**.
    4. Valige **Valemi redigeerimine**.
    5. Valige valemiredaktoris **Parameetrid**.
    6. Konfigureeritud avaldisele parameetrite määramiseks toimige järgmiselt.

        1. Valige suvand **Uus**.
        2. Sisestage dialoogiboksis väljale **Nimi** väärtus **Argument**.
        3. Valige väljal **Tüüp** andmetüüp **Kahendmuutuja**.
        4. Valige nupp **OK**.

    7. Sisestage väljale **Valem** väärtus **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")**, et tagastada asjakohase ER-i sildi tekst, võttes arvesse käivitamise konteksti keelt ja määratletud parameetri väärtust.
    8. Valige **Salvesta** ja sulgege seejärel valemiredaktor.
    9. Uue andmeallika lisamiseks valige **OK**.

![Konfigureeritud mudelivastendus ER-i mudelivastenduse kujundajas](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Andmeallikate sidumine andmemudeli väljadega

Peate siduma konfigureeritud andmeallikad andmemudeli väljadega, et määrata, kuidas andmemudelisse käitusajal rakenduse andmeid lisatakse.

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmemudel** suvand **CompanyName**.
2. Laiendage paanil **Andmeallikad** suvand **CompanyInfo** ja järgige neid juhiseid.

    1. Laiendage sõlm **CompanyInfo.find()**, mis tähistab tabeli CompanyInfo meetodit **find()**.
    2. Valige **CompanyInfo.find().Name**.
    3. Valige **Seo**, et täita selle ettevõtte nimi, mille jaoks kutsutakse käitusajal konfigureeritud mudelivastendust.

3. Valige paanil **Andmemudel** suvand **Küsimustik**.
4. Valige paanil **Andmeallikad** suvand **Küsimustik** ja seejärel **Seo**, et täita küsimustiku kirjed.
5. Laiendage paanil **Andmemudel** suvand **Küsimustik** ja järgige neid juhiseid.

    1. Valige paanil **Andmemudel** suvand **Aktiivne**.
    2. Valige paanil **Andmemudel** suvand **Redigeeri**.
    3. Sisestage väljale **Valem** väärtus **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)**, et täita loetelu väärtuste võrdluse tulemus, mis sõltub tekstist ja keelest.

6. Jätkake samal viisil andmeallikate sidumist andmemudeli väljadega, kuni saavutate järgmise tulemuse.

    | Välja tee                                              | Andmetüüp   | Tegevus | Siduv avaldis |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | String      | Seo   | CompanyInfo.'find()'.Name |
    | Küsimustik                                           | Kirjete loend | Seo   | Küsimustik |
    | Questionnaire\\Active                                   | String      | Redigeeri   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Questionnaire\\Code                                     | String      | Seo   | \@.kmCollectionId |
    | Questionnaire\\Description                              | String      | Seo   | \@.Description |
    | Questionnaire\\QuestionnaireType                        | String      | Seo   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Questionnaire\\QuestionOrder                            | String      | Redigeeri   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",<br>EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | Questionnaire\\ResultsGroup                             | Salvestamine      |        | |
    | Questionnaire\\ResultsGroup\\Code                       | String      | Seo   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Questionnaire\\ResultsGroup\\Description                | String      | Seo   | \@.'\$ResultGroup'.description |
    | Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Tegelik        | Seo   | \@.'\$ResultGroup'.maxPoint |
    | Questionnaire\\Question                                 | Kirjete loend | Seo   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Questionnaire\\Question\\CollectionSequenceNumber       | Täisarv     | Seo   | \@.answerCollectionSequenceNumber |
    | Questionnaire\\Question\\Id                             | String      | Seo   | \@.kmQuestionId |
    | Questionnaire\\Question\\MustBeCompleted                | String      | Redigeeri   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\PrimaryQuestion                | String      | Seo   | \@.parentQuestionId |
    | Questionnaire\\Question\\SequenceNumber                 | Täisarv     | Seo   | \@.SequenceNumber |
    | Questionnaire\\Question\\Text                           | String      | Seo   | \@.'\$Question'.text |
    | Questionnaire\\Question\\Answer                         | Kirjete loend | Seo   | \@.'\$Question'.'\$Answer' |
    | Questionnaire\\Question\\Answer\\CorrectAnswer          | String      | Redigeeri   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\Answer\\Points                 | Tegelik        | Seo   | \@.point |
    | Questionnaire\\Question\\Answer\\SequenceNumber         | Täisarv     | Seo   | \@.sequenceNumber |
    | Questionnaire\\Question\\Answer\\Text                   | String      | Seo   | \@.text |

    Järgmisel illustratsioonil on kujutatud konfigureeritud mudelivastenduse lõplik olek lehel **Mudelivastenduse kujundaja**.

    ![Täiesti konfigureeritud mudelivastendus ER-i mudelivastenduse kujundajas](./media/er-quick-start1-mapping2.png)

7. Salvestage muudatused.
8. Sulgege leht **Mudelivastenduse kujundaja**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Mudelivastenduse kujunduse lõpuleviimine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku vastendamine**.
3. Valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.
4. Valige **Muuda olekut** \> **Lõpule viidud**.

Selle konfiguratsiooni versiooni 1.1 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**. Versiooni 1.1 ei saa enam muuta. See versioon sisaldab konfigureeritud mudelivastendust ja seda saab kasutada teiste ER-i konfiguratsioonide alusena. Luuakse selle konfiguratsiooni versioon 1.2, mille olek on **Mustand**. Saate seda versiooni redigeerida, et kohandada konfiguratsiooni **Küsimustiku vastendamine**.

![Redigeeritava ER-i konfiguratsiooni versioonid lehel „Konfiguratsioonid”](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Konfigureeritud mudelivastendus esindab äridomeeni **Küsimustik** esindava abstraktse andmemudeli rakenduse Finance põhist juurutamist.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Kohandatud aruande malli kujundamine

ER-i raamistik kasutab eelmääratletud malle, et luua aruandeid Microsoft Office'i vormingutes (Exceli töövihikud või Wordi dokumendid). Vajaliku aruande loomisel täidetakse mall konfigureeritud andmevoo järgi vajalike andmetega. Seetõttu peate esmalt kujundama oma kohandatud aruande jaoks malli. See mall peab olema kujundatud Exceli töövihikuna, mille struktuur esindab kohandatud aruande paigutust. Peate panema nime kõikidele Exceli üksustele, mida kavatsete täita vajalike andmetega.

1. Laadige alla fail [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) ja salvestage see oma kohalikku arvutisse.
2. Avage fail Excelis ja vaadake üle töövihiku struktuur.

Nagu järgmisel illustratsioonil näha, on allalaaditud mall loodud printima määratud küsimustikke, mis esitavad küsimustiku küsimused koos asjakohaste vastustega.

![Exceli mall määratud küsimustike printimiseks](./media/er-quick-start1-template-layout.png)

Küsimustiku üksikasjade täitmiseks on sellele mallile lisatud Exceli nimed. Exceli nimede ülevaatamiseks saate kasutada nimehaldurit.

![Nimehalduri kasutamine Exceli nimede ülevaatamiseks esitatud Exceli mallis](./media/er-quick-start1-template-names.png)

Aruande sildid on lisatud inglise keeles fikseeritud tekstina. Saate asendada aruande sildid uute Exceli nimedega, mis täidavad keelest sõltuva tekstiga sildid, kasutades ER-i vormingu [silte](#AddMmLabels), nagu tegite konfigureeritud mudelivastenduse puhul keelest sõltuvate avaldiste korral. Sel juhul tuleb ER-i sildid lisada redigeeritavas ER-i vormingus.

Nagu järgmisel illustratsioonil näha, on kohandatud aruande päist muudetud, et lisada leheküljenumbrid Excelis.

![Kohandatud aruande päis esitatud Exceli mallis](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Vormingu kujundamine

Elektroonilise aruandluse funktsionaalse konsultandi rollis kasutajana peate looma uue ER-i konfiguratsiooni, mis sisaldab [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponenti. Peate konfigureerima vormingu komponendi, et määrata, kuidas sisestatakse vajalikud andmed käitusajal aruandemalli.

Kui täidate jaotises [Kujundatud vormingu konfiguratsiooni importimine](#FormatImport) toodud juhised, saate vajaliku vormingu importida esitatud XML-failist. Teise võimalusena saate täita jaotise [Uue vormingu konfiguratsiooni loomine](#FormatCreate) juhised, et kujundada see vorming täiesti algusest.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Kujundatud vormingu konfiguratsiooni importimine

1. Laadige alla fail [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) ja salvestage see oma kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.
5. Valige **Sirvi** ning seejärel otsige üles ja valige fail **Questionnaires format.version.1.1.xml**.
6. Konfiguratsiooni importimiseks valige **OK**.

Jätkamiseks jätke järgmine protseduur [Uue vormingu konfiguratsiooni loomine](#FormatCreate) vahele.

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Uue vormingu konfiguratsiooni loomine
 
1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku mudel**.
3. Valige **Konfiguratsiooni loomine**.
4. Dialoogiakna ripploendis järgige allolevaid etappe.

    1. Valige väljal **Uus** suvand **Küsimustike andmemudelil põhinev vorming**.
    2. Sisestage väljale **Nimi** tekst **Küsimustiku aruanne**.
    3. Valige väljal **Andmemudeli versioon** väärtus **1**.

        > [!NOTE]
        > - Kui valite kindla põhiandmemudeli versiooni, ühtib andmemudeli asjakohase versiooni struktuur loodavas vormingus andmeallika **Mudel** struktuuriga.
        > - Võite selle välja tühjaks jätta. Sellisel juhul ühtib andmemudeli versiooni **Mustand** struktuur loodavas vormingus andmeallika **Mudel** struktuuriga. Seejärel saate kohandada oma mudelit ja näha neid korrigeerimisi oma vormingus. See meetod võib parandada ER-i lahenduse kujunduse tõhusust, kui konfigureerite oma andmemudeli, mudelivastenduse ja vormingu samal ajal.
        > - Kui valite põhiandmemudeli kindla versiooni, saate hiljem vormingut redigeerides aktiveerida versiooni **Mustand**.

    4. Valige väljal **Andmemudeli definitsioon** definitsioon **Juur**.

5. Konfiguratsiooni loomiseks valige **Loo konfiguratsioon**.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Aruandemalli importimine

1. Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku aruanne**.
2. Valige **Kujundaja**, et alustada kohandatud vormingu konfigureerimist.
3. Valige lehe **Vormingu kujundaja** toimingupaanil suvand **Impordi** \> **Impordi Excelist**.
4. Järgige dialoogiboksis järgmiseid juhiseid.

    1. Valige **Lisa mall**.
    2. Otsige üles ja valige kohalikult salvestatud fail **Questionnaires report template.xslx** ning seejärel valige **Ava**.
    3. Malli importimiseks valige **OK**.

    ![Aruandemalli importimine](./media/er-quick-start1-template-import.png)

Vorminguelement **Excel\\File** lisatakse automaatselt juurelemendina redigeeritavasse vormingusse. Lisaks lisatakse automaatselt kõikide imporditud mallis tuvastatud Exceli nimede jaoks kas vorminguelement **Excel\\Range** või **Excel\\Cell**. Vorming **Excel\\Header**, millel on pesastatud element **String**, lisatakse automaatselt, et kajastada imporditud malli päisesätteid.

![Automaatselt lisatud elemente sisaldava vormingu struktuur ER-i toimingute kujundajas](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Vormingu konfigureerimine

1. Valige lehel **Vormingu kujundaja** vormingupuus juurelement **Excel**.
2. Sisestage lehe paremal pool vahekaardi **Vorming** väljale **Nimi** väärtus <a name="AddFormatRootElement"></a>**Report**.
3. Valige väljal **Keele-eelistus** suvand **Kasutaja eelistus**, et käitada aruanne kasutaja eelistatud keeles.
4. Valige väljal **Kultuurieelistus** suvand **Kasutaja eelistus**, et käitada aruanne kasutaja eelistatud kultuuris.

    Lisateavet ER-i protsessi jaoks keele- ja kultuurikontekstide määramise kohta leiate teemast [Mitmekeelsete aruannete kujundamine](er-design-multilingual-reports.md).

    ![Kujundatud aruande jaoks keele- ja kultuurisätete konfigureerimine ER-i toimingute kujundajas](./media/er-quick-start1-template-format-structure1.png)

5. Laiendage vormingupuul juursõlm ja valige **ResultsGroup**.
6. Valige vahekaardil **Vorming** väljal **Edastamise suund** suvand **Edastust pole**, kuna te ei eelda, et ühe küsimustiku jaoks on mitu tulemusegruppi.

    ![Edastamise suuna määramine vahemiku vorminguelementide jaoks ER-i toimingute kujundajas](./media/er-quick-start1-template-format-structure2.png)

7. Valige käsk **Salvesta**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Andmesidumise määratlemine aruande pealkirja jaoks

Peate määrama vorminguelemendi jaoks andmesidumise, mida kasutatakse loodud aruande pealkirja täitmiseks.

1. Valige lehel **Vormingu kujundaja** parempoolsel vahekaardil **Vastendus** element **Report\\ReportTitle**.
2. Valige **Valemi redigeerimine**.
3. Valige valemiredaktoris **Tõlgi**.
4. Järgige dialoogiboksis **Teksti tõlkimine** allolevaid etappe.

    1. Sisestage väljale **Sildi ID** väärtus **ReportTitle**.
    2. Sisestage väljale **Tekst vaikekeeles** väärtus **Küsimustike aruanne**.
    3. Valige **Tõlgi** ja seejärel suvand **Salvesta**.
    4. Valige **Tõlgi**, et sulgeda dialoogiboks **Teksti tõlkimine**.

5. Sulgege valemiredaktor.

    ![Seose konfigureerimine loodud aruande pealkirja täitmiseks](./media/er-quick-start1-add-report-title-label.png)

Saate kasutada seda meetodit, et muuta kõik muud praeguse malli sildid keelest sõltuvaks. Lisateavet selle kohta, kuidas ühe ER-i konfiguratsiooni lisatud silte saab tõlkida kõikidesse toetatud keeltesse, leiate teemast [Mitmekeelsete aruannete kujundamine](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Mudeli andmeallika ülevaatamine

1. Valige lehel **Vormingu kujundaja** vahekaardil **Vastendus** andmeallikas <a name="ModelDSName"></a>**mudel**, mis esindab selle ER-i vormingu põhiandmemudelit.
2. Valige suvand **Redigeeri**.
3. Vaadake üle dialoogiboksis **Andmeallika atribuudid** olev teave. See andmeallikas tähistab andmeallika komponendi **Küsimustikud** versiooni 1, mis asub ER-i konfiguratsioonis **Küsimustike mudel**.

![Mudeli andmeallika atribuudid ER-i toimingute kujundajas](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Vorminguelementide sidumine andmeallika väljadega

Et määrata, kuidas mall käitusajal täidetakse, peate siduma iga vorminguelemendi, mis on seotud asjakohase Exceli nimega, selle vormingu andmeallika ühe väljaga.

1. Valige lehel **Vormingu kujundaja** vormingupuus vorminguelement **Report\\CompanyName**.
2. Valige vahekaardil **Vastendus** andmeallika väli **model.CompanyName**, mille tüüp on **String**.
3. Valige **Seo**, et sisestada malli ettevõtte nimi.
4. Valige vormingupuus element **Report\\Questionnaire**.
5. Valige vahekaardil **Vastendus** andmeallika väli **model.Questionnaire**, mille tüüp on **Kirjete loend**.
6. Valige **Seo**.
7. Valige **Kuva üksikasjad**, et näha vorminguelementide üksikasju.

    Vahemiku vorminguelement **Küsimustik** konfigureeritakse vertikaalselt edastavana. Kui see seotakse andmeallikaga, mille tüüp on **Kirjete loend**, korratakse Exceli malli asjakohast vahemikku **Küsimustik** seotud andmeallika iga kirje puhul.
 
    ![Vahemiku vorminguelemendi „Küsimustik” sidumine asjakohaste kirjete loendi tüüpi andmeallikatega ER-i toimingute kujundajas](./media/er-quick-start1-bindings1.png)

    Kuna Exceli malli vahemik **Küsimustik** on määratletud ridades 5 kuni 14, korratakse neid ridu iga esitatud küsimustiku puhul.

    ![Exceli malli read, mida korratakse loodud aruandes kirjete loendi tüüpi andmeallikate kõikide kirjete puhul](./media/er-quick-start1-template-questionnaire-range.png)

8. Konfigureerige samasugused seosed ülejäänud vorminguelementide jaoks, nagu kirjeldatud järgmises tabelis.

    > [!NOTE]
    > Selles tabelis eeldatakse veerus „Andmeallika tee” oleva teabe puhul, et ER-i funktsioon [suhteline tee](relative-path-data-bindings-er-models-format.md) on sisse lülitatud.

    | Vorminguelemendi tee                                      | Andmeallika tee |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Questionnaire                                     | **model.Questionnaire** |
    | Excel\\Questionnaire\\Active                             | **\@.Active**, kus **\@** on **model.Questionnaire** |
    | Excel\\Questionnaire\\Code                               | **\@.Code** |
    | Excel\\Questionnaire\\Description                        | **\@.Description** |
    | Excel\\Questionnaire\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Questionnaire\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Questionnaire\\ResultsGroup\\Code\_               | **\@.ResultsGroup.Code** |
    | Excel\\Questionnaire\\ResultsGroup\\Description\_        | **\@.ResultsGroup.Description** |
    | Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Questionnaire\\Question                           | **\@.Question** |
    | Excel\\Questionnaire\\Question\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, kus **\@** on **model.Questionnaire.Question** |
    | Excel\\Questionnaire\\Question\\Id                       | **\@.Id** |
    | Excel\\Questionnaire\\Question\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Questionnaire\\Question\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Questionnaire\\Question\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Questionnaire\\Question\\Text                     | **\@.Text** |
    | Excel\\Questionnaire\\Question\\Answer                   | **\@.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer    | **\@.CorrectAnswer**, kus **\@** on **model.Questionnaire.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\Points           | **\@.Points** |
    | Excel\\Questionnaire\\Question\\Answer\\Text             | **\@.Text** |

9. Kui olete lõpetanud, valige **Salvesta**.

Järgmisel illustratsioonil on kujutatud konfigureeritud andmesidumiste lõplik olek lehel **Vormingu kujundaja**.

![Konfigureeritud andmesidumised ER-i toimingute kujundajas](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Terve määratud andmeallikate ja sidumiste kogum tähistab konfigureeritud vormingu vorminguvastenduse komponenti. Seda vorminguvastendust kutsutakse, kui käivitate aruande loomiseks konfigureeritud vormingu.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Kujundatud vormingu käivitamine ER-is

Saate nüüd kujundatud vormingu lehel **Konfiguratsioonid** testimiseks käivitada.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehel **Konfiguratsioon** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku aruanne**.
3. Valige **Kujundaja** vormingu versiooni jaoks, mille olek on **Mustand**.
4. Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.
5. Konfigureerige dialoogiboksis **ER-i parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.
6. Valige filtreerimissuvandi kinnitamiseks **OK**.
7. Aruande käivitamiseks valige **OK**.
8. Vaadake loodud aruanne üle.

[Vaikimisi](electronic-reporting-destinations.md#default-behavior) on loodud aruanne Exceli failis, mille saate alla laadida. Järgmistel illustratsioonidel on kujutatud Exceli vormingus loodud aruande kaks lehekülge.

![Exceli vormingus loodud aruande näide, lehekülg 1](./media/er-quick-start1-report1a.png)

![Exceli vormingus loodud aruande näide, lehekülg 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Kujundatud vormingu häälestamine

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Vormingu muutmine loodud dokumendi nime muutmiseks

Loodud dokumendile pannakse vaikimisi nimi praeguse kasutaja pseudonüümi põhjal. Vormingut muutes saate seda funktsiooni muuta nii, et loodud dokumendile pannakse nimi teie kohandatud loogika põhjal. Näiteks võib loodud dokumendi nimi põhineda praeguse seansi kuupäeval ja kellaajal ning aruande pealkirjal.

1. Valige lehel **Vormingu kujundaja** juurüksus **Aruanne**.
2. Valige vahekaardil **Vastendus** suvand **Redigeeri faili nime**.
3. Sisestage väljale **Valem** väärtus **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.
4. Valige **Salvesta** ja sulgege seejärel valemiredaktor.
5. Valige käsk **Salvesta**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Vormingu muutmine küsimuste järjekorra muutmiseks

Küsimused ei ole loodud aruandes õiges järjekorras. Järjekorra muutmiseks saate muuta vormingut.

1. Valige lehel **Vormingu kujundaja** juurüksus **Aruanne**.
2. Laiendage vahekaardil **Vastendus** vormingupuus suvand **Report\\Questionnaire\\Question**.

    ![Vahemiku tüüpi küsimuse vorminguelement ER-i toimingute kujundajas](./media/er-quick-start1-bindings3.png)

3. Valige vahekaardil **Vastendus** suvand **model.Questionnaire**.
4. Valige **Lisa** \> **Funktsioonid\\Arvutatud väli** ja seejärel sisestage väljale **Nimi** väärtus **OrderedQuestions**.
5. Valige **Valemi redigeerimine**.
6. Sisestage valemiredaktoris väljale **Valem** väärtus **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)**, et järjestada praeguse küsimustiku küsimuste loend järjekorranumbri alusel.
7. Valige **Salvesta** ja sulgege seejärel valemiredaktor.
8. Valige **OK**, et lõpetada uue arvutatud välja sisestamine.
9. Valige vahekaardil **Vastendus** suvand **model.Questionnaire.OrderedQuestions**.
10. Valige vormingupuul **Excel\\Questionnaire\\Question**.
11. Valige **Seo** ja seejärel kinnitage, et praegune tee **model.Questionnaire.Questions** vahetatakse pesastatud elementide kõikides seostes uue tee **model.Questionnaire.OrderedQuestions** vastu.
12. Valige käsk **Salvesta**.

![Küsimuse vorminguelemendi sidumine konfigureeritud andmeallikaga OrderedQuestions ER-i toimingute kujundajas](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Muudetud vormingu käivitamine ER-is

Nüüd saate muudetud vormingu testimiseks ER-i raamistikus käivitada.

1. Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.
2. Konfigureerige dialoogiboksis **ER-i parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.
3. Valige filtreerimissuvandi kinnitamiseks **OK**.
4. Aruande käivitamiseks valige **OK**.
5. Vaadake loodud aruanne üle.

Järgmisel illustratsioonil on näha Exceli vormingus loodud aruanne, kus küsimused on õiges järjekorras.

![Exceli vormingus loodud aruanne, mille küsimused on õiges järjekorras](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Vormingu kujunduse lõpuleviimine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku aruanne**.
3. Valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.
4. Valige **Muuda olekut** \> **Lõpule viidud**.

Selle konfiguratsiooni versiooni 1.1 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**. Versiooni 1.1 ei saa enam muuta. See versioon sisaldab konfigureeritud vormingut ja seda saab kasutada kohandatud aruande printimiseks. Luuakse selle konfiguratsiooni versioon 1.2, mille olek on **Mustand**. Saate seda versiooni redigeerida, et kohandada aruande **Küsimustik** vormingut.

![Redigeeritava ER-i konfiguratsiooni versioonid lehel „Konfiguratsioonid”](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Konfigureeritud vorming moodustab aruande **Küsimustik** kujunduse ja see pole seotud Finance'i-põhiste artefaktidega.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Rakenduse artefaktide arendamine kujundatud aruande kutsumiseks

Süsteemiadministraatori rollis kasutajana peate arendama välja uue loogika, et konfigureeritud ER-i vormingut saaks kutsuda rakenduse kasutajaliidesest (UI) kohandatud aruande loomiseks. Praegu ei paku ER seda tüüpi loogika konfigureerimiseks ühtegi võimalust. Seetõttu on vaja teha natuke tehnilist tööd. 

Uue loogika arendamiseks peate juurutama topoloogia, mis toetab pidevat järku. Lisateavet leiate teemast [Pidevat järku ja testimise automatiseerimist toetavate topoloogiate juurutamine](../perf-test/continuous-build-test-automation.md). Samuti peab teil selle topoloogia puhul olema juurdepääs arenduskeskkonnale. Lisateavet saadaval ER-i API kohta leiate teemast [ER-i raamistiku API](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Lähtekoodi muutmine

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Andmelepingu klassi lisamine

Lisage oma Microsoft Visual Studio projekti uus klass **QuestionnairesErReportContract** ja kirjutage kood, mis määrab, millist andmelepingut tuleks konfigureeritud ER-i vormingu käivitamiseks kasutada.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>UI-koostaja klassi lisamine

Lisage uus klass **QuestionnairesErReportUIBuilder** oma Visual Studio projekti ja kirjutage kood, et luua käitusaja dialoogiboks, mida kasutatakse käivitatava ER-i vormingu vorminguvastenduse ID ülesleidmiseks. Esitatud kood otsib ainult ER-i vorminguid, mis sisaldavad andmeallikat, mille tüüp on **Andmemudel**, ning mis viitab andmemudelile **[Küsimustikud](#DataModeName)**, kasutades definitsiooni **[Juur](#RootDefinitionName)**.

> [!NOTE]
> Teise võimalusena saate ER-i vormingute filtreerimiseks kasutada ER-i integratsioonipunkte. Lisateavet leiate teemast [API vorminguvastenduse otsingu kuvamiseks](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Andmepakkuja klassi lisamine

Lisage oma Microsoft Visual Studio projekti uus klass **QuestionnairesErReportDP** ja kirjutage kood, mis määrab andmepakkuja, keda tuleks konfigureeritud ER-i vormingu käivitamiseks kasutada. Esitatud kood hõlmab selle andmepakkuja puhul ainult andmelepingut.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Siltide faili lisamine

Lisage uus siltide fail **QuestionnairesErReportLabels\_en-US** oma Visual Studio projekti ja määrake uute kasutajaliidese ressursside jaoks järgmised sildid.

- Silt **\@QuestionnairesReport** uue menüüelemendi jaoks, mis sisaldab USA inglise keeles (en-US) järgmist teksti: **Küsimustike aruanne (ER-i põhine)**
- Silt **\@QuestionnairesReportBatchJobDescription** pakett-töö pealkirja jaoks, kui valitud ER-i vorming on pakett-tööna käivitamiseks ajastatud

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Aruandeteenuse klassi lisamine

Lisage uus klass **QuestionnairesErReportService** oma Visual Studio projekti ja kirjutage kood, mis kutsub ER-i vormingut, tuvastab selle vorminguvastenduse ID abil ja esitab parameetrina andmelepingu.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Kui peate kasutama ER-i vormingut, mis käitab rakenduse andmeid, peate vorminguvastenduses konfigureerima andmeallika, mille tüüp on **Andmemudel**. See andmeallikas viitab määratud andmemudeli kindlale osale, kasutades ühte juurdefinitsiooni. ER-i vormingu käivitamisel kutsub see andmeallikat, et saada juurdepääs asjakohasele ER-i mudelivastendusele, mis on konfigureeritud asjaomase mudeli ja juurdefinitsiooni jaoks.

Kogu teavet, mida te lähtekoodis ette valmistate ja andmelepingu osana talletate, saab edastada töötavale ER-i vormingule, kasutades seda tüüpi ER-i mudelivastendust. ER-i mudelivastenduses peate konfigureerima andmeallika, mille tüüp on **Objekt** ja mis viitab klassile **[QuestionnairesErReportContract](#DataContractClass)**. Mudelivastenduse tuvastamiseks peate määrama andmeallika, mis kutsub seda mudelivastendust. Esitatud koodis on see andmeallikas täpsustatud konstanti **ERModelDataSourceName** abil, mille väärtus on **[mudel](#ModelDSName)**. Et tuvastada, millist andmeallikat kasutatakse mudelivastenduses andmelepingu paljastamiseks, peate määrama andmeallika nime. Esitatud koodis on see nimi täpsustatud konstanti **ParametersDataSourceName** abil, mille väärtus on <a name="DataContractDSName"></a>**RunTimeParameters**.

> [!NOTE]
> Uues keskkonnas peate võib-olla värskendama ER-i metaandmeid, et seda tüüpi klass oleks ER-i mudelivastenduse kujundajas saadaval. Lisateavet leiate teemast [ER-i raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Aruandekontrolleri klassi lisamine

Lisage uus klass **QuestionnairesErReportController** oma Visual Studio projekti ja kirjutage kood, mis käitab ER-i vormingu teie eelistuste põhjal kas sünkroonses või pakktöötlusrežiimis dialoogiboksis, mis on kujundatud klassis **QuestionnairesErReportUIBuilder** leiduva loogika põhjal.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Menüüelemendi lisamine

Lisage uus menüüelement **QuestionnairesErReport** oma Visual Studio projekti. Atribuudis **Objekt** viitab see menüüelement klassile **QuestionnairesErReportController** ning seda kasutatakse kasutajaõiguse määramiseks ER-i vormingu valimiseks ja käivitamiseks. Atribuudis **Silt** viitab see menüüelement varem loodud sildile **\@QuestionnairesReport**, nii et rakenduse kasutajaliideses kuvatakse õige tekst.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Menüüelemendi lisamine menüüle

Lisage olemasolev menüü **KM** oma Visual Studio projekti. Peate sellesse menüüsse lisama uue üksuse **QuestionnairesErReport**, mille tüüp on **Väljund**. See üksus peab viitama menüüelemendile **QuestionnairesErReport**, mida kirjeldatakse eelmises jaotises.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Visual Studio projekti koostamine

Koostage oma projekt, et muuta uus menüüelement kasutajatele kättesaadavaks.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Vormingu käivitamine rakenduses

1. Avage **Küsimustik** \> **Kujundus** \> **Küsimustike aruanne (ER-i põhine)**.

    ![Menüüelemendi „Küsimustike aruanne (ER-i põhine)” valimine küsimustiku moodulis, et käivitada konfigureeritud ER-i vorming](./media/er-quick-start1-application-menu-modified.png)

2. Valige dialoogiboksis **Vorminguvastendus** suvand **Küsimustike aruanne**.
3. Valige nupp **OK**.
4. Konfigureerige dialoogiboksis **Elektroonilise aruande parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.
5. Valige filtreerimissuvandi kinnitamiseks **OK**.
6. Aruande käivitamiseks valige **OK**.

    ![Valikukriteeriumide täpsustamine elektroonilise aruande dialoogiboksis](./media/er-quick-start1-report-run-dialog-page.png)

7. Vaadake loodud aruanne üle.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Kujundatud ER-i lahenduse häälestamine

Saate muuta konfigureeritud ER-i lahendust nii, et see kasutaks andmepakkuja klassi, mille arendasite töötava ER-i vormingu üksikasjadele juurdepääsemiseks, ja nii, et see sisestaks selle ER-i vormingu nime loodud aruandesse.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Mudelivastenduse muutmine

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Andmeallikate lisamine andmelepingu objektile juurdepääsemiseks

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku vastendamine**.
3. Valige **Kujundaja**, et avada leht **Mudelist andmeallikasse vastendamine**.
4. Valige **Kujundaja**, et avada valitud vastendus mudelivastenduse kujundajas.
5. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Objekt**.
6. Valige paanil **Andmeallikad** suvand **Lisa juur**.
7. Sisestage dialoogiboksis väljale **Nimi** väärtus **[RunTimeParameters](#DataContractDSName)**, nagu on määratletud klassi **QuestionnairesErReportService** lähtekoodis.
8. Sisestage väljale **Klass** väärtus **[QuestionnairesErReportContract](#DataContractClass)**, mille kood kirjutati varem.
9. Valige nupp **OK**.
10. Laiendage suvand **RunTimeParameters**.

Lisatud andmeallikas annab teavet töötava ER-i vorminguvastenduse kirje ID kohta.

![Lisatud andmeallikas ER-i mudelivastenduse kujundajas](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Andmeallika lisamine ER-i vorminguvastenduse kirjetele juurdepääsemiseks

Jätkake valitud mudelivastenduse redigeerimist andmeallika lisamise kaudu, et pääseda juurde ER-i vorminguvastenduse kirjetele.

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.
2. Valige paanil **Andmeallikad** suvand **Lisa juur**.
3. Sisestage dialoogiboksis väljale **Nimi** väärtus **ER1**.
4. Sisestage väljale **Tabel** väärtus **ERFormatMappingTable**.
5. Valige nupp **OK**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Andmeallika lisamine töötava ER-i vorminguvastenduse kirjele juurdepääsemiseks

Jätkake valitud mudelivastenduse redigeerimist andmeallika lisamise kaudu, et pääseda juurde töötava ER-i vormingu vorminguvastenduse kirjele.

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.
2. Valige paanil **Andmeallikad** suvand **Lisa juur**.
3. Sisestage dialoogiboksis väljale **Nimi** väärtus **ER2**.
4. Valige **Valemi redigeerimine**.
5. Sisestage valemiredaktoris väljale **Valem** väärtus **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.
6. Valige **Salvesta** ja sulgege seejärel valemiredaktor.
7. Valige nupp **OK**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Töötava ER-i vormingu nime sisestamine andmemudelisse

Jätkake valitud mudelivastenduse redigeerimist, et töötava ER-i vormingu nimi sisestataks andmemudelisse.

1. Laiendage lehel **Mudelivastenduse kujundaja** paanil **Andmemudel** suvand **ExecutionContext** ja seejärel valige **ExecutionContext\\FormatName**.
2. Valige paanil **Andmemudel** suvand **Redigeeri**, et konfigureerida valitud andmemudeli välja jaoks andmesidumine.
3. Sisestage valemiredaktoris väljale **Valem** väärtus **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.
4. Valige **Salvesta** ja sulgege seejärel valemiredaktor.

Kuna kasutasite välja **FormatName**, siis paljastab konfigureeritud mudelivastendus nüüd ER-i vormingu nime, mis kutsub käivitamise ajal seda mudelivastendust.

![Andmemudeli välja sidumine lisatud andmeallika meetodiga ER-i mudelivastenduse kujundajas](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Mudelivastenduse kujunduse lõpuleviimine

1. Valige lehel **Mudelivastenduse kujundaja** suvand **Salvesta**.
2. Sulgege leht.
3. Sulgege mudelivastenduste leht.
4. Veenduge lehe **Konfiguratsioonid** konfiguratsioonipuus, et konfiguratsioon **Küsimustiku vastendamine** oleks endiselt valitud. Siis valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.
5. Valige **Muuda olekut** \> **Lõpule viidud**.

Selle konfiguratsiooni versiooni 1.2 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**. Versiooni 1.2 ei saa enam muuta. See versioon sisaldab konfigureeritud mudelivastendust ja seda saab kasutada teiste ER-i konfiguratsioonide alusena. Luuakse selle konfiguratsiooni versioon 1.3, mille olek on **Mustand**. Saate seda versiooni redigeerida, et kohandada mudelivastendust **Küsimustik**.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Vormingu muutmine

Saate muuta konfigureeritud ER-i vormingut nii, et selle nimi kuvataks ER-i vormingu käivitamisel loodava aruande jaluses.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Uue vorminguelemendi lisamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku aruanne**.
3. Valige **Kujundaja**.
4. Valige lehel **Vormingu kujundaja** juurüksus **Aruanne**.
5. Valige **Lisa**, et lisada uus pesastatud vorminguelement valitud juurüksusele **Aruanne**.
6. Valige **Excel\\Footer**.
7. Sisestage väljale **Nimi** väärtus **Footer**.
8. Valige **Report\Footer** ja seejärel **Lisa**.
9. Valige **Text\\String**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Lisatud vorminguelemendi sidumine

1. Valige lehel **Vormingu kujundaja** vahekaardil **Vastendus** vormingupuus aktiivse elemendi **Jalus\\String** puhul suvand **Redigeeri valemit**.
2. Sisestage valemiredaktoris väljale **Valem** väärtus **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.
3. Valige **Salvesta** ja sulgege seejärel valemiredaktor.
4. Valige käsk **Salvesta**.

Konfigureeritud vormingut on nüüd muudetud nii, et selle nimi sisestatakse loodud aruande jalusesse, kasutades elementi **Footer\\String**.

![Jaluse vorminguelemendi lisamine konfigureeritud vormingusse ER-i toimingute kujundajas](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Vormingu kujunduse lõpuleviimine

1. Sulgege **Vormingu kujundaja** leht.
2. Veenduge lehe **Konfiguratsioonid** konfiguratsioonipuus, et konfiguratsioon **Küsimustiku aruanne** oleks endiselt valitud. Siis valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.
3. Valige **Muuda olekut** \> **Lõpule viidud**.

Selle konfiguratsiooni versiooni 1.2 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**. Versiooni 1.2 ei saa enam muuta. See versioon sisaldab konfigureeritud vormingut ja seda saab kasutada teiste ER-i konfiguratsioonide alusena. Luuakse selle konfiguratsiooni versioon 1.3, mille olek on **Mustand**. Saate seda versiooni redigeerida, et kohandada aruannet **Küsimustik**.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Vormingu käivitamine rakenduses

1. Avage **Küsimustik** \> **Kujundus** \> **Küsimustike aruanne (ER-i põhine)**.
2. Valige dialoogiboksis **Vorminguvastendus** suvand **Küsimustike aruanne**.
3. Valige nupp **OK**.
4. Konfigureerige dialoogiboksis **ER-i parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.
5. Valige filtreerimissuvandi kinnitamiseks **OK**.
6. Aruande käivitamiseks valige **OK**.
7. Vaadake loodud fail Exceli vormingus üle.

Pange tähele, et loodud aruande jalus sisaldab aruande loomiseks kasutatud ER-i vormingu nime.

![Loodud fail Exceli vormingus](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Vormingu käivitamine ER-is

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku aruanne**.
3. Valige toimingupaanil käsk **Käivita**.
4. Konfigureerige dialoogiboksis **Elektroonilise aruande parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.
5. Valige filtreerimissuvandi kinnitamiseks **OK**.
6. Aruande käivitamiseks valige **OK**.
7. Vaadake loodud fail Exceli vormingus üle.

Pange tähele, et loodud aruande jalus ei sisalda aruande loomiseks kasutatud ER-i vormingu nime, kuna andmelepingu objekti ei edastatud töötavasse mudelivastendusse, kui seda kutsus ER-is käivitatud ER-i vorming.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Vormingu sihtkoha konfigureerimine ekraanil eelvaatamiseks

1. Avage **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse sihtkoht**.
2. Lisage lehel **Elektroonilise aruandluse sihtkoht** konfigureeritud ER-i vormingu **Küsimustiku aruanne** jaoks sihtkoha kirje.
3. Seadistage kiirkaardil **Faili sihtkoht** [sihtkoht](er-destination-type-screen.md) **Ekraan** vormingu komponendi **Aruanne** jaoks, mis on [lisatud](#AddFormatRootElement) konfigureeritud ER-i vormingu **Küsimustiku aruanne** juurelemendina.
4. Konfigureerige kiirkaardil **PDF-i teisenduse sätted** sihtkoht, et teisendada aruanne [PDF-vormingusse](electronic-reporting-destinations.md#OutputConversionToPDF), mis kasutab lehe paigutust **Horisontaalne**.

![Elektroonilise aruandluse sihtkoha lehel ER-i vormingu jaoks kohandatud sihtkoha „Ekraan” konfigureerimine](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Vormingu käivitamine rakenduses selle eelvaatamiseks PDF-dokumendina

1. Avage **Küsimustik** \> **Kujundus** \> **Küsimustike aruanne (ER-i põhine)**.
2. Valige dialoogiboksis **Vorminguvastendus** suvand **Küsimustike aruanne**.
3. Valige nupp **OK**.
4. Konfigureerige dialoogiboksis **Elektroonilise aruande parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.
5. Valige filtreerimissuvandi kinnitamiseks **OK**.

    Pange tähele, et kiirkaardil **Sihtkohad** on välja **Väljund** väärtuseks seatud **Ekraan**. Kui soovite konfigureeritud sihtkohta muuta, valige **Muuda**.

    ![ER-i aruande käitusaja dialoogiboks, kus saate muuta konfigureeritud sihtkohta](./media/er-quick-start1-run-settings.png)

6. Aruande käivitamiseks valige **OK**.
7. Vaadake loodud fail PDF-vormingus üle.

    ![PDF-vormingus loodud aruande eelvaade ekraanil](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse valemi keel](er-formula-language.md)
- [Mitmekeelsete aruannete kujundamine](er-design-multilingual-reports.md)
- [ER-raamistiku API](er-apis-app73.md)
- [Funktsioon CASE](er-functions-logical-case.md)
- [Funktsioon CONCATENATE](er-functions-text-concatenate.md)
- [Funktsioon DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [Funktsioon FILTER](er-functions-list-filter.md)
- [Funktsioon FIRSTORNULL](er-functions-list-firstornull.md)
- [Funktsioon FORMAT](er-functions-text-format.md)
- [Funktsioon IF](er-functions-logical-if.md)
- [Funktsioon ORDERBY](er-functions-list-orderby.md)
- [Funktsioon SESSIONNOW](er-functions-datetime-sessionnow.md)
