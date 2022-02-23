---
title: Vöötkoodi andmeallikate kasutamine vöötkoodipiltide loomiseks
description: Selles teemas selgitatakse, kuidas kasutada vöötkoodi andmeallikaid vöötkoodipiltide loomiseks.
author: NickSelin
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: 3fb754267de1120bc3c086d49cb7c63028183bda
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681420"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Vöötkoodi andmeallikate kasutamine vöötkoodipiltide loomiseks

[!include[banner](../includes/banner.md)]

Saate kasutada [elektroonilise aruandluse (ER)](general-electronic-reporting.md) raamistikku, et kujundada [ER-i vormingukomponente](general-electronic-reporting.md#FormatComponentOutbound), mida saate käitada vajalike elektrooniliste ja prinditavate väljaminevate dokumentide loomiseks. Väljamineva dokumendi loomiseks Microsoft Office'i vormingus peate määrama aruande paigutuse, kasutades aruandemallina kas Microsoft Exceli dokumenti või Microsoft Wordi dokumenti. [ER-i toimingute koostaja](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) võimaldab teil manustada ER-i vormingu jaoks mallina Exceli või Wordi dokumendi. Järgmised lisatud mallis olevad nimega elemendid on seostatud konfigureeritud vormingukomponendi elementidega.

- Sisu juhtelemendid Wordis
- Nimega lehed, vahemikud, lahtrid, kujundid ja pildid Excelis

Neid nimega elemente kasutatakse kohatäitena andmete jaoks, mis sisestatakse ER-i vormingu käitamisel loodud dokumenti. ER-i vorminguelemendid on seotud andmeallikatega. Need andmeallikad määratlevad andmed, mis sisestatakse loodud dokumentidesse käitamise ajal. Lisateavet vt teemast [Piltide ja kujundite manustamine ER-i abil loodud dokumentides](electronic-reporting-embed-images-shapes.md).

ER toetab nüüd andmeallika tüüpi **Vöötkood**. Seetõttu saate nüüd luua pildi, mis tähistab konkreetse teksti vöötkoodi. ER-i vormingu konfigureerimisel saate vöötkoodipiltide loomiseks määrata andmeallikad, mille tüüp on **Vöötkood**. Seejärel saate lisada need pildid loodud äridokumentidesse, nagu tellimused, arved, saatelehed ja kviitungid. Saate lisada need ka erinevatele siltidele, nagu toote- ja riiulisildid ning pakkimis- ja saadetise sildid.

Aruandemallides saab kasutada vöötkoodipiltide sisestamiseks järgmiseid kohatäiteid.

- [Pildi](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word)sisu juhtelement Wordi jaoks
- [Pildi](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344)objekt Excelis

Kasutades andmeallikat, mille tüüp on **Vöötkood**, saate luua vöötkoode järgmistes vormingutes.

- Ühemõõtmelised vöötkoodid:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Intelligent Mail
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Kahemõõtmelised vöötkoodid:

    - Aztec
    - Data Matrix
    - QR-kood

**Vöötkoodi** andmeallika konfigureerimisel saate määratleda kindlad renderdamisparameetrid, mida kasutatakse pildi loomiseks.

- **Laius** – määrake vöötkoodi laius pikslites. Väärtus **0** (null) tähendab, et kasutatakse vaikelaiust. Tähendus võib eri vormingute puhul varieeruda.
- **Kõrgus** – määrake vöötkoodi kõrgus pikslites. Väärtus **0** (null) tähendab, et kasutatakse vaikekõrgust. Tähendus võib eri vormingute puhul varieeruda.
- **Veeris** – määrake vöötkoodi veerise suurus pikslites. Veeris viitab vöötkoodi mõlemal küljel olevale alale, mis tuleb hoida tühjana (nn puhver). Väärtus **0** (null) tähendab, et kasutatakse vaikeveerist. Tähendus võib eri vormingute puhul varieeruda.
- **Väljundi sisu** – seadke väärtuseks **Jah**, et luua vöötkoodipilt, mis sisaldab kodeeritud teavet tekstina. Vaikeväärtus on **Ei**.
- **Kodeering** – määrake loodud vöötkoodipildis kodeeritavate märkide tüüp. Vaikimisi kasutatakse **UTF-8** kodeeringut.

> [!IMPORTANT]
> Uue **Vöötkoodi** andmeallika lisamisel peate selle asetama pesastatud elemendina mõne muu üksuse (konteineri) alla.
>
> Kui seote andmellika **Vöötkood** vormingus lahtrielemendiga ning lahtrielement tähistab Wordi sisu juhtelementi või Exceli pilti, esitatakse andmeallikas selles seoses funktsioonina, millel on üks parameeter, mille tüüp on **String**. Peate seda parameetrit kasutama, et määrata tekst, mis tuleb muuta vöötkoodipildiks ja mida loetakse vöötkoodi skannimisel.

Selle funktsiooni kohta lisateabe saamiseks läbige siinse teema näited.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Näide: tšeki loomine, mis sisaldab vöötkoodi, millesse on kodeeritud tasumisele kuuluv summa

Selles näites on näha, kuidas **süsteemiadministraatori** või **elektroonilise aruandluse funktsionaalse konsultandi** rolliga kasutaja saab konfigureerida ER-i vormingu, mis sisaldab malli, mida kasutatakse vöötkoodi sisaldava väljamineva dokumendi loomiseks Exceli vormingus. Siin on ülevaade vajalikest toimingutest.

1. [Eeltingimuste täitmine](#ExamplePrerequisites).
2. [Konfiguratsioonipakkuja aktiveerimine](#ExampleProvider).
3. [Pakutava ER-i lahenduse importimine](#ExampleImportSolution).
4. [Tšeki loomine](#ExampleGenerateCheque).
5. [Loodud tšeki ülevaatamine](#ExampleReviewGeneratedCheque).
6. [Pakutava ER-i lahenduse vormingu muutmine](#ExampleModifyFormat).

    1. [Uue tšekimalli rakendamine](#ExampleModifyFormatApplyTemplate).
    2. [Uue vöötkoodi andmeallika lisamine](#ExampleModifyFormatAddDataSource).
    3. [Uue vorminguelemendi sidumine](#ExampleModifyFormatBindFormatElement).
    4. [Muudetud versiooni kättesaadavaks tegemine testkäivitusteks](#ExampleModifyFormatMakeVersionAvailable).

        1. [Muudetud vorminguversiooni lõpule viimine](#CompleteToRun).
        2. [Mustandiversiooni kättesaadavaks tegemine kasutamiseks](#MarkToRun).

7. [Tšeki loomine](#ExampleGenerateCheque2).
8. [Loodud tšeki teisendamine PDF-iks](#ExampleConvertToPDF).

Selles näites kasutatakse tšekkide loomiseks konfigureeritud pakutavat ER-i lahendust. See lahendus loob tšekid, millel esitatakse tasumisele kuuluv summa nii numbri kui ka tekstina. Te muudate ER-i lahendust nii, et tšekk sisaldaks ka loodud vöötkoodi, kuhu on kodeeritud tasumisele kuuluv summa ja mida saab lugeda vöötkoodiskanneri abil.

Neid toimingud saab lõpule viia **USMF** ettevõttes rakenduses Microsoft Dynamics 365 Finance.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Eeltingimuste täitmine

Selle näite läbimiseks peab teil olema juurdepääs rakendusele USMF ettevõttele rakenduses Finance ühega järgmistest rollidest.

- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

Kui te pole veel lõpule viinud näidet teemas [Piltide ja kujundite manustamine ER-i abil loodud dokumentides](electronic-reporting-embed-images-shapes.md), laadige alla järgmised ER-i näidislahenduse konfiguratsioonid.

| Sisu kirjeldus         | Faili nimi                   |
|-----------------------------|-----------------------------|
| ER-i andmemudeli konfiguratsioon | Model for cheques.xml       |
| Elektroonilise aruandluse vormingu konfiguratsioon     | Cheques printing format.xml |

Lisaks laadige alla järgmine Exceli fail, mis sisaldab muudetud malli pakutava ER-i lahenduse jaoks.

| Sisu kirjeldus | Faili nimi                 |
|---------------------|---------------------------|
| Aruandemall     | Check template Excel.xlsx |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Konfiguratsioonipakkuja aktiveerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Veenduge lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad**, et näidisettevõtte **Litware, Inc.** [konfiguratsioonipakkuja](general-electronic-reporting.md#Provider) oleks loendis ja aktiivseks märgitud. Kui seda pole loendis või kui see pole märgitud aktiivseks, järgige juhiseid teemas [Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Näidisettevõtte märkimine aktiivseks lokaliseerimise konfiguratsioonide lehel](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Pakutava ER-i lahenduse importimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.
3. Kui lehel **Konfiguratsioonid** pole konfiguratsioon **Tšekkide mudel** konfiguratsioonipuus saadaval, järgige ER-i andmemudeli konfiguratsiooni importimiseks järgmiseid samme.

    1. Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.
    2. Valige dialoogiboksis suvand **Sirvi**, otsige üles ja valige fail **Model for cheques.xml** ning seejärel valige **OK**.

4. Kui konfiguratsioonipuus pole konfiguratsioon **Tšekkide printimisvorming** saadaval, järgige ER-i vormingu konfiguratsiooni importimiseks järgmiseid samme.

    1. Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.
    2. Valige dialoogiboksis suvand **Sirvi**, otsige üles ja valige fail **Cheques printing format.xml** ning seejärel valige **OK**.

5. Laiendage konfiguratsioonipuus suvand **Tšekkide mudel**.
6. Vaadake imporditavate ER konfiguratsioonide loendit konfiguratsioonipuus.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Tšeki loomine

1. Avage jaotis **Sularaha- ja pangahaldus** \> **Pangakontod** \> **Pangakontod**.
2. Valige lehel **Pangakontod** konto **USMF OPER**.
3. Avage pangakonto üksikasjade lehel toimingupaanil vahekaart **Seadistamine** ning valige grupist **Paigutus** suvand **Tšekk**.
4. Valige lehel **Tšeki paigutus** suvand **Redigeeri**.
5. Seadke kiirkaardil **Üldine** suvandi **Üldine elektrooniline ekspordivorming** väärtuseks **Jah**.
6. Valige väljal **Ekspordivormingu konfiguratsioon** ER-i vorming **Tšekkide printimisvorming**, mille te enne importisite.
7. Valige toimingupaanil suvand **Prindi test**.
8. Seadke dialoogiboksis suvandi **Käibiv tšekivorming** väärtuseks **Jah** ja valige seejärel **OK**.

    ![Tšeki paigutuse ja testi printimise dialoogiboks](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Loodud tšeki ülevaatamine

- Avage loodud tšekk Excelis.
2. Vaadake loodud tšekk üle.

    ![Loodud tšekk Excelis](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Pakutava ER-i lahenduse vormingu muutmine

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Uue tšekimalli rakendamine

Varem imporditud faili **Cheque template Excel.xlsx** avamiseks saate kasutada Exceli töölauarakendust. Pange tähele, et see mall erineb mallist, mida kasutasite tšeki loomiseks pakutud ER-i lahenduses. Lisaks sisaldab see vöötkoodipildi elementi **AmountBarcode**.

![Element AmountBarcode Exceli mallis](./media/er-barcode-data-source-cheque2.png)

Nüüd peate muutma ER-i lahendust ja seejärel muudetud malli [uuesti rakendama](modify-electronic-reporting-format-reapply-excel-template.md).

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** suvand **Aruandluse konfiguratsioonid**.
3. Laiendage lehel **Konfiguratsioonid** konfiguratsioonipuus suvand **Tšekkide mudel** ja valige **Tšekkide printimisvorming**.
4. Valige toimingupaanil valik **Koostaja**.
5. Valige ER-i toimingute koostajas lehe parempoolsest servast vahekaart **Vastendamine** ja klõpsake siis vasakul oleva vormingupuu paanil suvandit **Laienda/ahenda**.
6. Pange tähele, et kõik lahtrivormingu elemendid on seotud sobivate andmeallikatega.

    ![ER-i toimingute koostajas lahtrivormingu elementide sidumine andmeallikatega](./media/er-barcode-data-source-cells-bound.png)

7. Valige lehe parempoolsest servast vahekaart **Vorming**.
8. Valige toimingupaanil kolmikpunkt (**...**) ja seejärel **Impordi**.
9. Valige grupis **Impordi** suvand **Värskenda Excelist** ja seejärel suvand **Värskenda malli**.
10. Leidke dialoogiboksis teie arvutisse salvestatud fail **Cheque template Excel.xlsx**, valige see ja klõpsake seejärel **OK**, et kinnitada valitud malli rakendamine.
11. Valige lehe parempoolsest servast vahekaart **Vastendamine** ja klõpsake siis vasakul oleva vormingupuu paanil suvandit **Laienda/ahenda**.
12. Pange tähele, et lahtrielement **AmountBarcode** on vormingusse lisatud. See element on seotud elemendiga **AmountBarcode**, mis on lisatud vöötkoodipildi kohatäitena muudetud Exceli malli.

    ![ER-i toimingute koostajas vormingule lisatud lahtrielement AmountBarcode](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Uue vöötkoodi andmeallika lisamine

Järgmisena tuleb lisada uus andmeallikas, mille tüüp on **Vöötkood**.

1. Valige ER-i toimingute loojas vahekaardil **Vastendamine** lehe parempoolsest servast **printimise** andmeallikas.
2. Valige **Lisa** ja seejärel grupis **Funktsioonid** andmeallika tüüp **Vöötkood**.

    ![Vöötkoodi andmeallika tüübi valimine](./media/er-barcode-data-source-add.png)

3. Sisestage dialoogiboksis väljale **Nimi** väärtus **vöötkood**.
4. Valige jaotises **Vöötkoodi vorming** suvand **Code 128**.
5. Sisestage väljale **Laius** väärtus **500**.
6. Valige nupp **OK**.

    ![Andmeallika atribuutide dialoogiboks](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Uue vorminguelemendi sidumine

Järgmisena peate siduma uue vorminguelemendi äsja lisatud andmeallikaga.

1. Valige ER-i toimingute loojas vahekaardil **Vastendamine** lehe parempoolsest servast andmeallikas **printimine\\vöötkood**.
2. Valige vasakul olevalt vormingupuu paanilt lahtrielement **AmountBarcode** ja klõpsake seejärel suvandit **Seo**.
3. Valige toimingupaanilt suvand **Kuva üksikasjad**.
4. Pange tähele, et kuna **Vöötkoodi** andmeallikas on seoses tähistatud üht parameetrit sisaldava funktsioonina, siis on seotud vorminguelemendi nimi võetud automaatselt selle parameetri argumendist.

    ![Vöötkoodi andmeallika üksikasjad ER-i toimingute kujundajas](./media/er-barcode-data-source-bind1.png)

5. Seose korrigeerimiseks valige **Redigeeri valemit**.

    Te ei soovi, et tagastataks lahtrielemendi nimi. Seetõttu peate konfigureerima avaldise, mis tagastab teksti, mis sisaldab praeguse tšeki tasumisele kuuluvat summat. Kuna emavahemik **ChequeLines** on seotud andmeallikaga **model.cheques**, siis on praeguse tšeki tasumisele kuuluv summa saadaval andmetüübi **Tegelik** väljal **model.cheques.attributes.amount**.

6. Sisestage väljale **Valem** väärtus **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.
7. Valige **Salvesta** ja sulgege seejärel [ER-i valemikoostaja](general-electronic-reporting-formula-designer.md).
8. Pange tähele, et seos on nüüd korrigeeritud.

    ![Korrigeeritud seos ER-i toimingute kujundajas](./media/er-barcode-data-source-bind2.png)

9. Valige **Salvesta** ja sulgege seejärel ER-i toimingute kujundaja.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Muudetud versiooni kättesaadavaks tegemine testkäivitusteks

Vaikimisi kasutatakse ER-i vormingu käitamisel ainult versioone, mille olek on **Lõpule viidud** ja **Jagatud**.

Kui olete muutmise lõpule viinud, saate praeguse mustandiversiooni kallal töötamise lõpetada ja teha oma muudatused kasutamiseks kättesaadavaks. Juhised leiate järgmisest jaotisest [Muudetud vorminguversiooni lõpule viimine](#CompleteToRun).

Kui soovite praeguse mustandiversiooni kallal tööd jätkata, kuid teil on vaja seda tšekkide loomiseks kasutada, peate selgelt määrama, et soovite käitamiseks kasutada vormingu mustandiversiooni. Juhised leiate jaotisest [Mustandiversiooni kättesaadavaks tegemine kasutamiseks](#MarkToRun).

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Muudetud vorminguversiooni lõpule viimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** suvand **Aruandluse konfiguratsioonid**.
3. Laiendage lehel **Konfiguratsioonid** konfiguratsioonipuus suvand **Tšekkide mudel** ja valige **Tšekkide printimisvorming**.
4. Valige kiirkaardil **Versioonid** kirje, mille olek on **Mustand**.
5. Valige **Muuda olekut** ja seejärel **Lõpule viidud**.
6. Valige dialoogiboksis **OK**.

Praeguse versiooni olek muudetakse olekust **Mustand** olekusse **Lõpule viidud** ning luuakse uus versioon, mille olek on **Mustand**. Te saate täiendavate muudatuste rakendamiseks kasutada uut mustandiversiooni.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Mustandiversiooni kättesaadavaks tegemine kasutamiseks

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** suvand **Aruandluse konfiguratsioonid**.
3. Avage lehe **Konfiguratsioonid** toimingupaanilt vahekaart **Konfiguratsioonid** ning valige grupist **Täpsemad sätted** suvand **Kasutaja parameetrid**.
4. Seadke dialoogiboksis suvandite **Käivita säte** väärtuseks **Jah** ja valige seejärel **OK**.
5. Laiendage konfiguratsioonipuus suvand **Tšekkide mudel** ja valige **Tšekkide printimisvorming**.
6. Seadke suvandi **Käivita säte** väärtuseks **Jah**.
7. Valige käsk **Salvesta**.

Valitud vormingu mustandiversioon on valitud vormingu käitamisel kasutamiseks saadaval.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Tšeki loomine

1. Avage jaotis **Sularaha- ja pangahaldus** \> **Pangakontod** \> **Pangakontod**.
2. Valige lehel **Pangakontod** konto **USMF OPER**.
3. Avage pangakonto üksikasjade lehel toimingupaanil vahekaart **Seadistamine** ning valige grupist **Paigutus** suvand **Tšekk**.
4. Valige lehe **Tšeki paigutus** toimingupaanilt suvand **Prindi test**.
5. Seadke dialoogiboksis suvandi **Käibiv tšekivorming** väärtuseks **Jah**.
6. Valige nupp **OK**.
7. Vaadake loodud tšekk üle. Pange tähele, et tšeki tasumisele kuuluva summa kodeerimiseks on loodud vöötkood.

    ![Loodud vöötkoodiga tšekk Excelis](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Kui **Vöötkoodi** andmeallika argument ei vasta selle vöötkoodi vormingule kehtivatele asjakohastele nõuetele, ilmneb tõrge. Näiteks kui **Vöötkoodi** andmeallikat kasutatakse [EAN-8](https://wikipedia.org/wiki/EAN-8) vöötkoodi loomiseks, ilmneb tõrge, kui tekst on pikem kui seitse tähemärki.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Loodud tšeki teisendamine PDF-iks

Nagu kirjeldatud teemas [Prinditavate FTI-vormide loomine](er-generate-printable-fti-forms.md#finland), saate loodud dokumendis vöötkoodide loomiseks kasutada spetsiaalset fonti. Sellisel juhul võib loodud dokumendi teisendamine hiljem sõltuda sellest, kas font on teisendamiskeskkonnas saadaval. Näiteks kui proovite teisendada dokumenti PDF-vormingusse või kuvada selle eelvaadet keskkonnas, kus font puudub, ei renderdata vöötkoode õigesti.

Kui aga kasutate vöötkoodide loomiseks **Vöötkoodi** andmeallikat, ei sõltu vöötkoodide renderdamine ühestki fondist. Seetõttu saate vöötkoode sisaldavaid dokumente hõlpsalt PDF-vormingusse teisendada. Järgmisel illustratsioonil on kujutatud loodud tšeki eelvaade, mis on [teisendatud](electronic-reporting-destinations.md#OutputConversionToPDF) PDF-iks konfigureeritud ER-i [sihtkoha](electronic-reporting-destinations.md) sätete alusel.

![Tšeki PDF-i eelvaade](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Kitsendused

> [!NOTE]
> Mõnel loodud vöötkooditüübil on fikseeritud proportsioonid. See on loogiline, kui olete sisse lülitanud funktsiooni **Luba EPPlusi teegi kasutamine elektroonilise aruandluse raamistikus**, et töötada ER-is Exceli dokumentidega. Sellisel juhul sisestatakse pilt kohatäitesse, millel on lukustatud proportsioonid. Kui malli kohatäite mõõtmed vastavad sisestatud pildi proportsioonide suhtele, võidakse loodud dokumendis tegeliku pildi suurust muuta, et säilitada vajalikud proportsioonid. Pildi suuruse muutmise takistamiseks kasutage kohatäidet, millel on soovitavad proportsioonid.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse sihtkohad](electronic-reporting-destinations.md)
- [Elektroonilise aruandluse valemi keel](er-formula-language.md)
- [Funktsioon NUMBERFORMAT](er-functions-text-numberformat.md)
