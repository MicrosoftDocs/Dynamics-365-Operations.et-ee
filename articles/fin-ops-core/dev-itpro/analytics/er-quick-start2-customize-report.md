---
title: ER-vormingu korrigeerimine kohandatud elektroonilise dokumendi loomiseks
description: Selles teemas selgitatakse, kuidas korrigeerida Microsofti elektroonilise aruandluse (ER) vormingut nii, et see looks kohandatud elektroonilise dokumendi.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7a32ac5f6ab21f89ed3c11c64458286864c9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680166"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>ER-vormingu korrigeerimine kohandatud elektroonilise dokumendi loomiseks

[!include[banner](../includes/banner.md)]

Selle teema protseduurid selgitavad, kuidas süsteemiadministraatori või elektroonilise aruandluse funktsionaalse konsultanti rolli kasutajad saavad neid ülesandeid täita.

- Parameetrite konfigureerimine [Elektroonilise aruandluse (ER) raamistiku jaoks](general-electronic-reporting.md).
- Importige ER-konfiguratsioonid, mida pakub Microsoft ja kasutatakse maksefaili loomiseks [hankija makse](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) töötlemise ajal.
- Looge standardse ER-vormingu konfiguratsiooni kohandatud versioon, mida pakub Microsoft.
- Muutke kohandatud ER-vormingu konfiguratsiooni nii, et see looks kindla panga nõuetele vastavad maksefailid.
- Võtke kasutusele muudatused, mis on tehtud standardsele ER-vormingu konfiguratsioonile kohandatud ER-vormingu konfiguratsioonis.

Kõiki järgmisi protseduure saab teha ettevõttes **GBSI**. Koodi pole vaja kirjutada.

- [ER-raamistiku konfigureerimine](#ConfigureFramework)

    - [Elektroonilise aruandluse parameetrite konfigureerimine](#ConfigureParameters)
    - [ER-konfiguratsiooni pakkuja aktiveerimine](#ActivateProvider)

        - [ER-konfiguratsiooni pakkujate loendi ülevaatamine](#ReviewProvidersList)
        - [Uue ER-vormingu konfiguratsioonipakkuja lisamine](#ActivateProvider)
        - [ER-konfiguratsiooni pakkuja aktiveerimine](#ActivateAddedProvider)

- [Standardse ER‑vormingu konfiguratsiooni importimine](#ImportERSolution1)

    - [Standardse ER-konfiguratsiooni importimine](#ImportERFormat1)
    - [Imporditud ER-konfiguratsioonide ülevaatamine](#ReviewImportedERSolution)

- [Hankija makse ettevalmistamine töötlemiseks](#PrepareVendorPayment)

    - [Hankija kontole panga teabe lisamine](#AddBankAccount)
    - [Hankija makse sisestamine](#EnterVendorPayment)

- [Hankija makse töötlemine standardse ER-vormingu abil](#ProcessVendorPayment1)

    - [Elektroonilise makseviisi seadistamine](#ConfigureMethodOfPayment1)
    - [Hankija makse töötlemine](#ProcessPayment1)

- [Standardse ER-vormingu kohandamine](#CustomizeProvidedFormat)

    - [Kohandatud vormingu loomine](#DeriveProvidedFormat)
    - [Kohandatud vormingu redigeerimine](#ConfigureDerivedFormat)
    - [Kohandatud vormingu märkimine käitatavaks](#MarkFormatRunnable)

- [Hankija makse töötlemine kohandatud ER-vormingu abil](#ProcessVendorPayment2)

    - [Elektroonilise makseviisi seadistamine](#ConfigureMethodOfPayment2)
    - [Hankija makse töötlemine](#ProcessPayment2)

- [Standardse ER‑vormingu konfiguratsiooni uute versioonide importimine](#ImportERSolution2)

    - [Standardse ER‑konfiguratsiooni uute versioonide importimine](#ImportERFormat2)
    - [Imporditud ER-vormingu konfiguratsioonide ülevaatamine](#ReviewImportedERFormat)

- [Muudatuste kasutuselevõtmine kohandatud vormingu imporditud vormingu uues versioonis](#AdoptNewBaseVersion)

    - [Kohandatud vormingu praeguse mustandversiooni lõpule viimine](#CompleteDerivedFormat)
    - [Uuele alusversioonile kohandatud vormingu aluse muutmine](#RebaseDerivedFormat)
    - [Hankija makse töötlemine muudetud alusega ER-vormingu abil](#ProcessPayment3)

- [Lisaressursid](#References)

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
> ER-konfiguratsiooni saab redigeerida ainult selle omanik. Seega enne ER-konfiguratsiooni redigeerimist pea olema tööruumis **Elektrooniline aruandlus** aktiveeriud vastav ER-konfiguratsiooni pakkuja.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER-konfiguratsiooni pakkujate loendi ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.
3. Lehel **Konfiguratsioonipakkuja tabel** on igal pakkuja kirjel kordumatu nimi ja URL. Vaadake üle selle lehe sisu. Kui üksuse **Litware, Inc.** (`https://www.litware.com`) kirje on juba olemas, jätke järgmine protseduur vahele [Uue ER-konfiguratsiooni pakkuja lisamine](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Uue ER-konfiguratsiooni pakkuja lisamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.
3. Lehel **Konfiguratsioonipakkujad** valige suvand **Uus**.
4. Väljale **Nimi** sisestage väärtus **Litware, Inc.**
5. Sisestage väljale **Interneti-aadress** `https://www.litware.com`.
6. Valige käsk **Salvesta**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>ER-konfiguratsiooni pakkuja aktiveerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Vailge lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Litware, Inc.** ja seejärel valige **Määra aktiivne**.

Lisateabe saamiseks ER-konfiguratsiooni pakkujate kohta vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Standardse ER‑vormingu konfiguratsiooni importimine

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Standardse ER-konfiguratsiooni importimine

Oma praegusesse Microsoft Dynamics 365 Finance'i eksemplari standardsete ER-konfiguratsioonide lisamiseks peate importima need selle eksemplari jaoks konfigureeritud ER-[hoidlast](general-electronic-reporting.md#Repository).

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Microsoft** ja seejärel valige pakkuja Microsoft hoidlate loendi kuvamiseks **Hoidlad**.
3. Valige lehel **Konfiguratsioonihoidlad** hoidla tüübiga **Globaalne** ja seejärel valige käsk **Ava**. Kui teilt küsitakse autoriseerimist ühenduse loomiseks Regulatory Configuration Service'iga, järgige autoriseerimise juhiseid.
4. Valige lehel **Konfiguratsioonihoidla** vasakpoolselt paanilt konfiguratsioonipuult vormingu **BACS (UK)** konfiguratsioon.
5. Kiirkaardil **Versioonid** valige valitud ER-vormingu konfiguratsiooni versioon **1.1**.
6. Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast alla Finance'i praegusesse eksemplari.

![Konfiguratsioonihoidla leht](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Kui teil on probleeme [globaalsele hoidlale](er-download-configurations-global-repo.md) juurde pääsemisega, saate selle asemel [laadida konfiguratsioonid alla](download-electronic-reporting-configuration-lcs.md) Microsoft Dynamics Lifecycle Servicesist (LCS).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Imporditud ER-konfiguratsioonide ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.
3. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel**.
4. Pange tähele, et lisaks valitud ER-vormingule **BACS (UK)** imporditi teised nõutavad ER-konfiguratsioonid. Veenduge, et konfiguratsioonipuus oleksid saadaval järgmised ER-konfiguratsioonid.

    - **Maksemudel** – see konfiguratsioon sisaldab [andmemudeli](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-komponenti, mis tähistab makse äridomeeni andmete struktuuri.
    - **Maksemudeli vastendamine 1611** – see konfiguratsioon sisaldab [mudeli vastendamise](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-komponenti, mis kirjeldab, kuidas andmemudel täidetakse rakenduse andmetega käitusajal.
    - **BACS (UK)** – see konfiguratsioon sisaldab [vormingu](general-electronic-reporting.md#FormatComponentOutbound) ja vormingu vastendamise ER-komponente. Vormingu komponent määratleb aruande paigutuse. Vormingu vastendamise komponent sisaldab mudeli andmeallikat ja määratleb, kuidas täidetakse aruande paigutust andmeallika abil käitusajal.

![Konfiguratsioonide leht](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Hankija makse ettevalmistamine töötlemiseks

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Hankija kontole panga teabe lisamine

Peate lisama hankija kontole panga teabe, millele viidatakse hiljem registreeritud makses.

1. Avage **Ostureskontro** \> **Hankijad** \> **Kõik hankijad**.
2. Valige lehel **Kõik hankijad** hankija konto **GB_SI_000001** ja seejärel valige toimingupaani vahekaardil **Hankija** grupis **Seadistamine** suvand **Pangakontod**.
3. Valige lehel **Hankija pangakontod** suvand **Uus** ja seejärel sisestage järgmine teave.

    1. Sisestage väljal **Pangakonto** suvand **GBP OPER**.
    2. Valige väljal **Pangagrupid** suvand **BankGBP**.
    3. Sisestage väljal **Pangakonto number** suvand **202015**.
    4. Sisestage väljale **SWIFT-kood** väärtus <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.
    5. Sisestage väljale **IBAN** väärtus **GB33BUKB20201555555555**.
    6. Jätke väljale **Registreerimisnumber** vaikeväärtus <a id="DefineRoutingNumber"></a>**123456**.

    ![Hankija pangakontode leht](./media/er-quick-start2-bank-account.png)

4. Valige käsk **Salvesta**.
5. Sulgege leht.
6. Avage lehel **Kõik hankijad** hankija konto **GB_SI_000001**.
7. Vajadusel valige hankija üksikasjade lehel **Redigeeri**, et muuta leht redigeeritavaks.
8. Valige kiirkaardi **Makse** väljal **Pangakonto** suvand **GBP OPER**.

    ![Hankija üksikasjade leht](./media/er-quick-start2-bank-account-reference.png)

9. Valige käsk **Salvesta**.
10. Sulgege leht.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Hankija makse sisestamine

Peate sisestama uue hankija makse [maksesoovituse](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal) abil.

1. Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.
2. Lehel **Hankija maksete tööleht** valige suvand **Uus**.
3. Valige väljal **Nimi** suvand **VendPay**.
4. Valige **Read**.
5. Valige **Maksesoovitus** \> **Loo maksesoovitus**.
6. Konfigureerige dialoogiboksis **Hankija maksesoovitus** filtreerimistingimused ainult hankija konto **GB_SI_000001** kirjete jaoks ja seejärel valige **OK**.
7. Valige arve **00000007_Inv** rida ja seejärel valige **Loo makse**.

    ![Hankija maksesoovituse dialoogiboks](./media/er-quick-start2-payment-proposal.png)

8. Veenduge, et sisestatud makse oleks konfigureeritud kasutama makseviisi **Elektrooniline**.

    ![Hankija maksete leht](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Hankija makse töötlemine standardse ER-vormingu abil

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Elektroonilise makseviisi seadistamine

Peate konfigureerima elektroonilise makseviisi, et see kasutaks imporditud ER-vormingu konfiguratsiooni.

1. Avage **Ostureskontro** \> **Maksmise seadistamine** \> **Makseviisid**.
2. Valige lehe **Makseviisid – hankijad** vasakpoolsel paanil makseviis **Elektrooniline**.
3. Valige suvand **Redigeeri**.
4. Seadistage kiirkaardil **Failivormingud** suvandi **Üldine elektrooniline ekspordivorming** väärtuseks **Jah**.
5. Valige väljal **Ekspordivormingu konfiguratsioon** vormingu konfiguratsioon **BACS (UK)**.

    ![Makseviisid - hankijate leht](./media/er-quick-start2-method-of-payment1.png)

6. Valige käsk **Salvesta**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Hankija makse töötlemine

1. Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.
2. Valige lehel **Hankija maksete tööleht** eelnevalt lisatud maksete tööleht ja seejärel valige **Read**.
3. Valige lehel **Hankija maksed** suvand **Loo maksed**.
4. Sisestage dialoogiboksi **Loo maksed** järgmine teave.

    - Valige väljal **Makseviis** **Elektrooniline**.
    - Valige väljal **Pangakonto** suvand **GBSI OPER**.

5. Valige nupp **OK**.
6. Määrake dialoogiboksis **Elektroonilise aruande parameetrid** suvandi **Prindi kontrollaruanne** väärtuseks **Jah** ja seejärel valige **OK**.

    ![Elektroonilise aruande parameetrite dialoogileht](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Lisaks maksefailile saate nüüd luua ka kontrollaruande.

7. Laadige alla ZIP-fail ja seejärel ekstraktige sellest järgmised failid.

    - Kontrollaruanne Exceli vormingus
    - Maksefail TXT-vormingus

        Pange tähele, et vastavalt antud ER-vormingu [struktuurile](#PositionRoutingNumber) algab loodud faili makserida registreerimisnumbriga, mis [määratleti](#DefineRoutingNumber) konfigureeritud pangakonto jaoks.

        ![Maksefail TXT-vormingus](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Standardse ER-vormingu kohandamine

Selles jaotises kuvatud näite puhul peaksite kasutama BACS-vormingus hankija maksete failide loomiseks Microsofti pakutavaid ER-konfiguratsioone, kuid peate lisama kohanduse, et toetada konkreetse panga nõudeid. Lisaks peaksite saama täiendada oma kohandatud vormingut, kui uued ER-konfiguratsioonide versioonid on saadaval. Kuid täiendust peaks olema võimalik teha madalaima hinnaga.

Sellisel juhul peaksite Litware, Inc.-i esindajana looma (tuletama) uue ER-vormingu konfiguratsiooni, kasutades alusena Microsofti antud konfiguratsiooni **BACS (UK)**.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Kohandatud vormingu loomine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **BACS (UK)**. Litware, Inc. kasutab kohandatud versiooni alusena selle ER-vormingu konfiguratsiooni versiooni 1.1.
3. Rippmenüü dialoogiboksi avamiseks valige käsk **Loo konfiguratsioon**. Selle dialoogiboksi abil saate luua uue konfiguratsiooni kohandatud maksevormingu jaoks.
4. Valige väljagrupis **Uus** suvand **Tuleta nimest: BACS (UK), Microsoft**.
5. Välja **Nimi** sisestage väärtus **BACS (UK kohandatud)**.

    ![Konfiguratsiooni loomise rippmenüü dialoogiaken](./media/er-quick-start2-add-derived-format.png)

6. Valige **Konfiguratsiooni loomine**.

Luuakse ER-vormingu konfiguratsiooni **BACS (UK kohandatud)** versioon 1.1.1. Selle versiooni [olek](general-electronic-reporting.md#component-versioning) on **Mustand** ja seda saab redigeerida. Teie kohandatud ER-vormingu praegune sisu vastab Microsofti antud vormingu sisule.

![Konfiguratsioonide leht](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Kohandatud vormingu redigeerimine

Peate konfigureerima oma kohandatud vormingut nii, et see vastaks pangapõhistele nõuetele. Näiteks võib pank nõuda, et loodavad maksefailid sisaldaksid SWIFT-koodi (Society for Worldwide Interbank Financial Telecommunication), millele määratakse agendi roll töödeldud hankija makses. SWIFT-koodid on rahvusvahelised pangakoodid, mis tuvastavad kindlad pangad üle maailma. Neid tuntakse ka panga identifikaatorkoodidena (BIC). SWIFT-kood peab sisaldama 11 märki ja see tuleb sisestada loodava maksefaili iga makserea algusesse.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **BACS (UK kohandatud)**.
3. Kiirkaardil **Versioonid** valige valitud konfiguratsiooni versioon **1.1.1**.
4. Valige **Kujundaja**.
5. Vorminguelementide kohta lisateabe saamiseks valige lehel **Vormingu koostaja** suvand **Kuva üksikasjad**.
6. Laiendage ja vaadake üle järgmised elemendid.

    - Tüübi **Kaust** element **BACSReportsFolder**. Seda elementi kasutatakse ZIP-vormingus väljundi loomiseks.
    - Tüübi **Fail** element **fail**. Seda elementi kasutatakse TXT-vormingus maksefaili loomiseks.
    - Tüübi **Järjestus** element **kanded**. Seda elementi kasutatakse maksefailis üksiku makserea loomiseks.
    - Tüübi **Järjestus** element **kanne**. Seda elementi kasutatakse üksiku makserea üksikute väljade loomiseks.

7. Valige element **kanne**.

    ![Kande element ER-toimingute koostajas](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Antud aruanne on konfigureeritud nii, et <a id="PositionRoutingNumber"></a>iga makserida algaks panga registreerimisnumbriga. Selleks otstarbeks kasutatakse vorminguelementi **VendBankRouteNum**. 

8. Valige **Lisa** ja seejärel valige lisatava vorminguelemendi tüüp **Tekst\\String**.

    1. Väljale **Nimi** sisestage väärtus **vendBankSWIFT**.
    2. Sisestage väljale **Minimaalne pikkus** väärtus **11**.
    3. Sisestage väljale **Maksimaalne pikkus** väärtus **11**.
    4. Valige nupp **OK**.

    > [!NOTE]
    > Elementi **VendBankSWIFT** kasutatakse hankija panga SWIFT-koodi sisestamiseks loodud failides.

9. Valige vormingustruktuuri puus **vendBankSWIFT**.
10. Valige **Nihuta üles**, et liigutada valitud vorminguelementi ühe taseme võrra ülespoole. Korrake seda etappi senikaua, kuni element **vendBankSWIFT** on <a id="PositionSWIFTCode"></a>esimene element peamise elemendi **kanne** all.

    ![VendBankSWIFT on ER-toimingute koostaja kande esimene element](./media/er-quick-start2-derived-format1.png)

11. Kui suvand **vendBankSWIFT** on vormingustruktuuri puus valitud, valige vahekaart **Vastendamine** ja seejärel laiendage andmeallikat **mudel**.
12. Laiendage suvandit **model.Payment** \> **model.Payment.CreditorAgent** ja valige andmeallika väli **model.Payment.CreditorAgent.BICFI**. See andmeallika väli näitab hankija panga SWIFT-koodi, millele määratakse agendi roll töödeldud hankija makses.
13. Valige **Seo**. Vorminguelement **VendBankSWIFT** on nüüd seotud andmeallika väljaga **model.Payment.CreditorAgent.BICFI**, et SWIFT-koode sisestatakse loodud maksefailidesse.

    ![Andmeallika väljaga model.Payment.CreditorAgent.BICFI seotud vorminguelement vendBankSWIFT ER-toimingute koostajas](./media/er-quick-start2-derived-format2.png)

14. Valige käsk **Salvesta**.
15. Sulgege koostaja leht.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Kohandatud vormingu märkimine käitatavaks

Kui teie kohandatud vormingu esimene versioon on loodud ja selle olek on **Mustand**, saate selle käitada testimise eesmärgil. Aruande käitamiseks peate töötlema hankija makset makseviisi abil, mis viitab teie kohandatud ER-vormingule. Kui toote rakendusest ER-vormingu võetakse vaikimisi [arvesse](general-electronic-reporting.md#component-versioning) ainult versioone, mille olek on **Lõpule viidud** või **Ühiskasutusse antud**. Selle käitumise abil saab vältida ER-vormingute kasutamist, mille koostamine on lõpetamata. Kuid oma testikäivitustel saate sundida rakendust kasutama teie ER-vormingu versiooni, mille olekuks on **Mustand**. Sedasi saate korrigeerida praeguse vormingu versiooni, kui muudatusi on vaja. Lisateavet vt jaotisest [Kohaldatavus](electronic-reporting-destinations.md#applicability).

ER-vormingu mustandversiooni kasutamiseks peate ER-vormingu selgelt märgistama.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Seadke dialoogiboksis **Kasutaja parameetrid** suvandi **Käivitamissätted** väärtuseks **Jah** ja valige seejärel **OK**.
4. Vastavalt vajadusele valige **Redigeeri**, et muuta praegune leht redigeeritavaks.
5. Valige vasakpoolse paani konfiguratsioonipuus **BACS (UK kohandatud)**.
6. Seadke suvandi **Käivita mustand** väärtuseks **Jah**.

    ![Suvand Käivita mustand lehel Konfiguratsioonid](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Hankija makse töötlemine kohandatud ER-vormingu abil

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Elektroonilise makseviisi seadistamine

Peate konfigureerima elektroonilise makseviisi, et teie kohandatud ER-vormingut kasutataks hankija maksete töötlemiseks.

1. Avage **Ostureskontro** \> **Maksmise seadistamine** \> **Makseviisid**.
2. Valige lehe **Makseviisid – hankijad** vasakpoolsel paanil makseviis **Elektrooniline**.
3. Valige suvand **Redigeeri**.
4. Seadistage kiirkaardil **Failivorming** suvandi **Üldine elektrooniline ekspordivorming** väärtuseks **Jah**.
5. Valige väljal **Ekspordivormingu konfiguratsioon** vormingu konfiguratsioon **BACS (UK kohandatud)**.

    ![Makseviisid - hankijate leht](./media/er-quick-start2-method-of-payment2.png)

6. Valige käsk **Salvesta**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Hankija makse töötlemine

1. Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.
2. Valige lehel **Hankija maksete tööleht** eelnevalt loodud maksete tööleht.
3. Valige **Read**.
4. Valige lehe **Hankija maksed** ruudustiku kohalt **Makse olek** \> **Puudub**.
5. Valige **Loo makse**.
6. Sisestage dialoogiboksi **Loo maksed** järgmine teave.

    - Valige väljal **Makseviis** **Elektrooniline**.
    - Valige väljal **Pangakonto** suvand **GBSI OPER**.

7. Valige nupp **OK**.
8. Määrake dialoogiboksis **Elektroonilise aruande parameetrid** suvandi **Prindi kontrollaruanne** väärtuseks **Jah** ja seejärel valige **OK**.

    > [!NOTE]
    > Lisaks maksefailile saate luua ainult kontrollaruande.

9. Laadige alla ZIP-fail ja seejärel ekstraktige sellest järgmised failid.

    - Kontrollaruanne Exceli vormingus
    - Maksefail TXT-vormingus

        Pange tähele, et vastavalt teie kohandatud ER-vormingu struktuurile [algab](#PositionSWIFTCode) loodud faili makserida nüüd SWIFT-koodiga, mis [sisestati](#DefineSWIFTCode) selle hankija pangakontole, kelle makse on töödeldud.

        ![Maksefail TXT-vormingus](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Standardse ER‑vormingu konfiguratsiooni uute versioonide importimine

Käesolevas jaotises kuvatud näite puhul kuvatakse teile teatis teabebaasi artikli [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046) kohta. Selle teatisega teavitatakse teid Microsofti avaldatud uuest ER-vormingu **BACS (UK)** versioonist. Lisaks kontrollaruandele võimaldab see uus versioon kasutajatel luua maksesoovituse aruannet ja osalemismärkuse aruannet hankija makse töötlemise ajal. Soovite hakata seda funktsiooni kasutama.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Standardse ER‑konfiguratsiooni uute versioonide importimine

Oma praegusesse Finance'i eksemplari ER-konfiguratsioonide uute versioonide lisamiseks peate importima need enda konfigureeritud ER-[hoidlast](general-electronic-reporting.md#Repository).

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Microsoft** ja seejärel valige pakkuja Microsoft hoidlate loendi kuvamiseks **Hoidlad**.
3. Valige lehel **Konfiguratsioonihoidlad** hoidla tüübiga **Globaalne** ja seejärel valige käsk **Ava**. Kui teilt küsitakse autoriseerimist ühenduse loomiseks Regulatory Configuration Service'iga, järgige autoriseerimise juhiseid.
4. Valige lehel **Konfiguratsioonihoidla** vasakpoolselt paanilt konfiguratsioonipuult vormingu **BACS (UK)** konfiguratsioon.
5. Kiirkaardil **Versioonid** valige valitud ER-vormingu konfiguratsiooni versioon **3.3**.
6. Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast alla Finance'i praegusesse eksemplari.

![Konfiguratsioonihoidla leht](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Kui teil on probleeme [globaalsele hoidlale](er-download-configurations-global-repo.md) juurde pääsemisega, saate selle asemel [laadida konfiguratsioonid alla](download-electronic-reporting-configuration-lcs.md) LCS-ist.

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Imporditud ER-vormingu konfiguratsioonide ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.
3. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **BACS (UK)**.
4. Kiirkaardil **Versioonid** valige versioon **3.3**.
5. Valige **Kujundaja**.
6. Laiendage lehel **Vormingu koostaja** vorminguelementi **BACSReportsFolder**.
7.  Pange tähele, et versioon 3.3 sisaldab vorminguelementi **PaymentAdviceReport**, mida kasutatakse maksesoovituse aruande loomiseks hankija makse töötlemisel.

    ![Vorminguelement PaymentAdviceReport ER-toimingute koostajas](./media/er-quick-start2-imported-solution2.png)

8. Sulgege koostaja leht.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Muudatuste kasutuselevõtmine kohandatud vormingu imporditud vormingu uues versioonis

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Kohandatud vormingu praeguse mustandversiooni lõpule viimine

Kui soovite jätta alles oma kohandatud vormingu praeguse oleku, viige lõpule mustandi versioon 1.1.1, muutes selle olek **Mustand** olekuks **Lõpule viidud**.

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.
3. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel**, laiendage **BACS (UK)** ja seejärel valige **BACS (UK kohandatud)**.
4. Valige kiirkaardil **Versioonid** **Muuda olekut** \> **Lõpuleviimine** ja seejärel valige **OK**.

Versiooni 1.1.1 olek **Mustand** muudetakse olekuks **Lõpule viidud** ja versioon muudetakse kirjutuskaitstuks. Lisatud on uus redigeeritav versioon, 1.1.2, ja selle olekuks on **Mustand**. Seda versiooni saate kasutada oma kohandatud ER-vormingu täiendavate muudatuste tegemiseks.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Uuele alusversioonile kohandatud vormingu aluse muutmine

Oma kohanduses vormingu **BACS (UK)** versiooni 3.3 uue funktsiooni kasutamiseks, peate muutma kohandatud konfiguratsiooni **BACS (UK kohandatud)** aluskonfiguratsiooni versiooni. Seda protsessi nimetatakse [aluse muutmiseks](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase). **BACS (UK)** versiooni 1.1 asemel kasutage uut versiooni 3.3.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **BACS (UK kohandatud)**.
3. Valige kiirkaardil **Versioonid** versioon **1.1.2** ja valige **Muuda alust**.
4. Valige dialoogiboksi **Muuda alust** väljal **Sihtversioon** aluskonfiguratsiooni versioon **3.3**, et rakendada see uue alusena ja kasutada seda konfiguratsiooni värskendamiseks.

    ![Dialoogiakna aluse muutmine](./media/er-quick-start2-rebase1.png)

5. Valige nupp **OK**.
6. Pange tähele, et mustandi versiooni number **1.1.2** on muudetud numbriks **3.3.2**, et kajastada alusversiooni muudatust.

    Kohandatud versiooni ja uue alusversiooni liitmisel võidakse avastada konflikte osade vormingumuudatuste tõttu, mida ei saa automaatselt ühendada.

    ![Muudetud alusega konfiguratsioon, millel on konflikte lehel Konfiguratsioonid](./media/er-quick-start2-rebase2.png)

    Konfliktide avastamisel tuleb need käsitsi lahendada vormingu koostajas.

7. Kiirkaardil **Versioonid** valige versioon **3.3.2**.
8. Valige **Kujundaja**.
9. Valige lehe **Vormingu koostaja** kiirkaardil **Üksikasjad** aluse muutmise konflikti kirje ja seejärel valige **Rakenda alusväärtus**.

    ![Aluse muutmise konflikti kirje ER-toimingute koostajas](./media/er-quick-start2-rebase3.png)

10. Valige käsk **Salvesta**.

    Aluse muutmise konflikti kirje ei tohiks olla enam kuvatud kiirkaardil **Üksikasjad**.

    ![Konflikt lahendatud ER-toimingute koostajas](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Lahendasite konflikti kinnitades, et selles ER-vormingus tuleb kasutada alusmudeli versiooni 3.

11. Laiendage suvandit **BACSReportsFolder** \> **fail** \> **kanded** \> **kanne**.
12. Pange tähele, et vahekaardil **Vastendamine** sisaldab teie kohandatud ER-vormingu versioon 3.3.2 nii teie kohandust (vorminguelementi **vendBankSWIFT** ja selle sidumist) kui ka Microsofti antud ER-vormingu aluse versiooni 3.3 uut funktsiooni (vorminguelementi **PaymentAdviceReport** koos selle pesastatud elementide ja konfigureeritud sidumistega). Vaid mõne hiireklõpsuga võtsite vastu uue alusversiooni muudatused, ühendades need oma kohandusega.

    ![Ühendatud vorming ER-toimingute koostajas](./media/er-quick-start2-rebase5.png)

13. Sulgege koostaja leht.

> [!NOTE]
> Aluse muutmise tegevus on tühistatav. Selle aluse muutmise tühistamiseks valige vahekaardil **Versioonid** vormingu **BACS (UK kohandatud)** versioon **1.1.1** ja seejärel valige **Hangi see versioon**. Versiooni 3.3.2 numbriks pannakse seejärel 1.1.2 ja mustandi versiooni 1.1.2 sisu vastab versiooni 1.1.1 sisule.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Hankija makse töötlemine muudetud alusega ER-vormingu abil

1. Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.
2. Valige lehel **Hankija maksete tööleht** eelnevalt loodud maksete tööleht.
3. Valige **Read**.
4. Valige lehe **Hankija maksed** ruudustiku kohalt **Makse olek** \> **Puudub**.
5. Valige **Loo makse**.
6. Sisestage dialoogiboksi **Loo maksed** järgmine teave.

    - Valige väljal **Makseviis** **Elektrooniline**.
    - Valige väljal **Pangakonto** suvand **GBSI OPER**.

7. Valige nupp **OK**.
8. Sisestage dialoogiboksi **Elektroonilise aruande parameetrid** järgmine teave.

    - Seadistage valik **Kontrollaruande printimine** olekusse **Jah**.
    - Seadistage valik **Maksesoovituse printimine** olekusse **Jah**.

    ![Elektroonilise aruande parameetrite dialoogiaken](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Lisaks maksefailile saate nüüd luua nii kontrollaruande kui ka maksesoovituse aruande.

9. Valige nupp **OK**.
10. Laadige alla ZIP-fail ja seejärel ekstraktige sellest järgmised failid.

    - Kontrollaruanne Exceli vormingus
    - Maksesoovituse aruanne Exceli vormingus

        ![Maksesoovituse aruanne Exceli vormingus](./media/er-quick-start2-payment-advice-report.png)

    - Maksefail TXT-vormingus

        Pange tähele, et loodud faili makserida algab SWIFT-koodiga, mis sisestati selle hankija pangakontole, kelle makse on töödeldud.

        ![Maksefail TXT-vormingus](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [ER-konfiguratsioonide allalaadimine teenusest Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [ER-konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]