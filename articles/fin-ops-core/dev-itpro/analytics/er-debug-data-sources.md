---
title: Käivitatud ER-vormingu andmeallikate silumine andmevoo ja teisenduse analüüsimiseks
description: Selles teemas selgitatakse, kuidas saate käivitatud ER-vormingu andmeallikaid siluda, et mõista paremini konfigureeritud andmevoogu ja teisendust.
author: NickSelin
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: fe3e6a4223fc8b26e523a982a2e1752a34b370de
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753668"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Käivitatud ER-vormingu andmeallikate silumine andmevoo ja teisenduse analüüsimiseks

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Kui [konfigureerite](tasks/er-format-configuration-2016-11.md) elektroonilise aruandluse (ER) lahendust väljaminevate dokumentide loomise otstarbel, siis määratlete andmete rakendusest kätte saamiseks ja saadud väljundi sisestamiseks kasutatavad meetodid. ER-lahenduse töötsükli toe tõhususe tagamiseks peaks teie lahendus sisaldama  [ER-andmemudelit](general-electronic-reporting.md#DataModelComponent) ja selle [vastendamise](general-electronic-reporting.md#ModelMappingComponent) komponente ning samuti [ER-vormingut](general-electronic-reporting.md#FormatComponentOutbound) ja selle vastendamise komponente, et tagada mudeli vastendamise rakenduspõhisus, samal ajal kui muud komponendid püsivad rakendusest sõltumatud. Seetõttu võivad loodud väljundisse andmete sisestamise protsessi [mõjutada ](general-electronic-reporting.md#FormatComponentOutbound) mitmesugused ER-komponendid.

Vahel näevad loodud väljundi andmed välja teistsugused kui samad andmed rakenduse andmebaasis. Sellisel juhul tuleks määratleda, milline ER-komponent vastutab andmeteisenduse eest. ER-andmeallika silurifunktsioon vähendab märkimisväärselt selle uurimiseks kuluvat aega ja kulusid. Saate katkestada ER-vormingu käitamise ja avada andmeallika siluri liidese. Seal saate kuvada saadaolevaid andmeallikaid ja valida käitamiseks konkreetse andmeallika. Käsitsi käitamine simuleerib andmeallika käitamist ER-vormingu tavapärase käitamise ajal. Tulemus esitatakse lehel, kus saate saadud andmeid analüüsida.

Andmeallika silumisfunktsiooni sisselülitamiseks seadke ER-i kasutajaparameetrite all suvandi **Luba vormingu käitamisel andmete silumine** sätteks **Jah** . Seejärel saate alustada andmeallika silumist, kui käivitate ER-vormingu väljaminevate dokumentide loomiseks. Lisaks saate kasutada suvandit **Alusta silumist**, et käivitada [ER-i toimingukoostajas](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document) konfigureeritud ER-vormingu andmeallika silumine.

Selles teemas antakse suunised täidetud ER-vormingute andmeallika silumise käivitamiseks. See selgitab, kuidas mõista teabe abil andmevoogu ja andmete teisendusi. Käesolevas teemas toodud näidetes kasutatakse hankija maksete töötlemise äriprotsessi.

## <a name="limitations"></a>Kitsendused

Andmeallika silurit saab kasutada väljaminevate dokumentide loomiseks käitatavate ER-vormingutes kasutatud andmeallikatele ligi pääsemiseks. Seda ei saa kasutada sissetulevate dokumentide sõelumiseks loodud ER-vormingute andmeallikate silumiseks.

Järgmised ER-vormingute sätted ei ole hetkel andmeallikate silumiseks kättesaadavad.

- Vormiteisendused
- Vormi ja vastendamise kinnitusreeglid
- Avaldiste lubamine
- Mälusisese andmekogumise üksikasjad

## <a name="prerequisites"></a>Eeltingimused

- Selles teemas toodud näidete läbimiseks peab teil olema juurdepääs ühele järgmistest [rollidest](../sysadmin/tasks/assign-users-security-roles.md).

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Ettevõtte sätteks peab olema seatud **DEMF**.

- Järgige käesoleva teema [1. lisas](#appendix1) toodud etappe, et laadida alla Microsofti ER-lahenduse komponendid, mis on vajalikud hankija maksete töötlemiseks.
- Järgige käesoleva teema [2. lisas](#appendix2) toodud etappe, et valmistada allalaaditavat ER-lahendust kasutades ostureskontro hankija maksete töötlemiseks ette.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Maksefaili saamiseks hankija makse töötlemine

1. Järgige käesoleva teema [3. lisas](#appendix3) toodud etappe, et töödelda hankija makseid.

    ![Hankija maksete töötlemine on pooleli](./media/er-data-debugger-process-payment.png)

2. Laadige alla ja salvestage zip-fail kohalikku arvutisse.
3. Ekstraktige zip-failist maksefail **ISO20022 Credit transfer.xml**.
4. Avage ekstraktitud maksefail XML-failide vaaturis.

    Maksefailis puuduvad hankija pangakonto rahvusvahelises pangakontonumbris (IBAN) tühikud. Seega erineb see lehel **Pangakontod** [sisestatud](#enteredIBANcode) väärtusest.

    ![Tühikuteta IBAN-kood](./media/er-data-debugger-payment-file.png)

    Saate kasutada ER-i andmeallika silurit, et saada teada, millist ER-lahenduse komponenti kasutatakse IBAN-koodi tühikute kärpimiseks.

## <a name="turn-on-data-source-debugging"></a>Andmeallika silumise sisselülitamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Määrake suvandi **Luba vormingu käitamisel andmete silumine** sätteks **Jah**.

    > [!NOTE]
    > See parameeter on kasutajakohane ja ettevõttekohane.

    ![Kasutaja parameetrite dialoogiaken](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Hankija makse töötlemine silumiseks

1. Järgige käesoleva teema [3. lisas](#appendix3) toodud etappe, et töödelda hankija makseid.
2. Valige teateaknas **Jah**, et kinnitada oma soov katkestada hankija makse töötlemine ja käivitada selle asemel lehel **Andmeallikate silumine** andmeallika silumine.

    ![Kinnituse teateaken](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Maksetöötluses kasutatavate andmeallikate silumine

### <a name="debug-the-model-mapping"></a>Mudeli vastendamise silumine

1. ER-komponendi silumise käivitamiseks valige lehekülje **Andmeallikate silumine** toimingupaanil suvand **Mudelivastendus**.
2. Valige vasakpoolselt andmeallikate paanilt andmeallikas **\$notSentTransactions** ja seejärel **Loe kõiki kirjeid**.

    Saate valida **Loe 1 kirje**, **Loe 10 kirjet**, **Loe 100 kirjet** või **Loe kõiki kirjeid**, et valida sobiv kirjete arv, mida valitud andmeallikas loetakse. Sel moel saate simuleerida andmetele juurdepääsu töötavast ER-vormingust.

3. Valige paremalt andmepaanilt suvand **Laienda kõik**.

    Näete, et **Kirje loetelu** tüübi kohta valitud andmeallikas sisaldub üks kirje.

4. Laiendage andmeallikas **\$notSentTransactions** ja valige pesastatud meetod **vendBankAccountInTransactionCompany()**.
5. Laiendage meetod **vendBankAccountInTransactionCompany()** ja seejärel valige pesastatud väli **IBAN**.
6. Valige **Too väärtus**.

    Saate valida suvandi **Too väärtus**, et sundkäivitada valitud andmeallika valitud välja väärtuse lugemine. Sel moel saate simuleerida antud väljale juurdepääsu töötavast ER-vormingust.

7. Valige **Laienda kõik**.

    ![IBAN-välja väärtus mudeli vastendamisel](./media/er-data-debugger-debugging-model-mapping.png)

    Nagu näete, ei vastuta mudelivastendus kärbitud tühikute eest, kuna tagastatav hankija pangakonto IBAN-kood sisaldab tühikuid. Seega peate jätkama andmeallika silumist.

### <a name="debug-the-format-mapping"></a>Vormingu vastendamise silumine

1. ER-komponendi silumise jätkamiseks valige lehekülje **Andmeallikate silumine** toimingupaanil suvand **Mudelivastendus**.
2. Valige **\$PaymentByDebtor** ja seejärel valige **Loe kõiki kirjeid**.
3. Laiendage **\$PaymentByDebtor**.
4. Laiendage **\$PaymentByDebtor.Lines** ja seejärel valige **Loe kõiki kirjeid**.
5. Laiendage **\$PaymentByDebtor.Lines.CreditorAccount**.
6. Laiendage **\$PaymentByDebtor.Lines.CreditorAccount.Identification** ja seejärel valige **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Valige **Too väärtus**.
8. Valige **Laienda kõik**.

    ![IBAN-välja väärtus vormingu vastendamisel](./media/er-data-debugger-debugging-format-mapping.png)

    Nagu näete, ei vastuta vorminguvastenduse andmeallikad kärbitud tühikute eest, kuna tagastatav hankija pangakonto IBAN-kood sisaldab tühikuid. Seega peate jätkama andmeallika silumist.

### <a name="debug-the-format"></a>Vormingu silumine

1. ER-komponendi silumise jätkamiseks valige lehekülje **Andmeallikate silumine** toimingupaanil suvand **Vorming**.
2. Laiendage vormingu elemendid, et valida **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**, ja seejärel valige **Loe kõiki kirjeid**.
3. Laiendage vormingu elemendid, et valida **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, ja seejärel valige **Loe kõiki kirjeid**.
4. Laiendage vormingu elemendid, et valida **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, ja seejärel valige **Too väärtus**.
5. Valige **Laienda kõik**.

    ![IBAN-välja väärtus vormingus](./media/er-data-debugger-debugging-format.png)

   Nagu näete, ei vastuta vormingu sidumine kärbitud tühikute eest, kuna tagastatav hankija pangakonto IBAN-kood sisaldab tühikuid. Seega on elementi **BankIBAN** konfigureeritud kasutama vorminguteisendust, mis kärbib tühikuid.

6. Sulgege andmeallika silur.

### <a name="review-the-format-transformations"></a>Vorminguteisenduste ülevaatus

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige leheküljel **Konfiguratsioonid** suvand **Maksemudel** \> **ISO20022 kreeditülekanne**.
3. Valige **Kujundaja** ja seejärel laiendage elemendid, et valida **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.

    ![BankIBAN element vormingukujundaja lehel](./media/er-data-debugger-referred-transformation.png)

    Nagu näete, on elementi **BankIBAN** konfigureeritud kasutama teisendust **eemalda mittetähtnumbrimärgid**.

4. Valige vahekaart **Teisendused**.

    ![BankIBAN elemendi teisenduste vahekaart](./media/er-data-debugger-transformation.png)

    Nagu näete, siis on teisendus **eemalda mittetähtnumbrimärgid** konfigureeritud kasutama avaldist, mis kärbib esitatud tekstistringist tühikud.

## <a name="start-to-debug-in-the-operation-designer"></a>Toimingukoostajas silumise käivitamine

Kui konfigureerite ER-vormingu mustandversiooni, mida saab käitada otse toimingukoostajas, siis pääsete ligi andmeallika silurile, valides toimingupaanilt **Alusta silumist**.

![Silumise alustamise nupp vormingu koostaja lehel](./media/er-data-debugger-run-from-designer.png)

Redigeeritava ER-vormingu vorminguvastendus ja vormingu komponendid on silumiseks kättesaadavad.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Mudelivastenduse koostajas silumise käivitamine

Kui konfigureerite ER-vormingu mudelivastendust, mida saab käitada lehel **Mudelivastendus**, siis pääsete ligi andmeallika silurile, valides toimingupaanilt **Alusta silumist**.

![Silumise alustamise nupp mudelivastenduse koostaja lehel](./media/er-data-debugger-run-from-designer-mapping.png)

Redigeeritava ER-vastenduse mudelivastenduse komponent on silumiseks kättesaadav.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>1. lisa: ER-lahenduse hankimine

### <a name="download-an-er-solution"></a>ER-lahenduse allalaadimine

Kui soovite töödeldava hankija makse kohta loodava elektroonilise maksefaili loomiseks kasutada ER-lahendust, siis saate [laadida alla](download-electronic-reporting-configuration-lcs.md) ER-maksevormingu **ISO20022 kreeditülekanne**, mis on kättesaadav rakenduse Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegis või globaalses hoidlas.

![ER-maksevormingu importimine konfiguratsiooni hoidla lehel](./media/er-data-debugger-import-from-repo.png)

Lisaks valitud ER-vormingule tuleb ER-lahenduse **ISO20022 kreeditülekanne** raames automaatselt Microsoft Dynamics 365 Finance'i eksemplari importida ka järgmised [konfiguratsioonid](general-electronic-reporting.md#Configuration).

- **Maksemudel** [ER-i andmemudeli konfiguratsioon](general-electronic-reporting.md#DataModelComponent)
- **ISO20022 kreeditülekanne** [ER-vormingu konfiguratsioon](general-electronic-reporting.md#FormatComponentOutbound)
- **Maksemudeli vastendamine 1611** [ER-mudeli vastendamise konfiguratsioon](general-electronic-reporting.md#ModelMappingComponent)
- **Maksemudeli vastendamine sihtkohta ISO20022** ER-mudeli vastendamise konfiguratsioon

Need konfiguratsioonid leiate ER-raamistiku lehelt **Konfiguratsioonid** (**Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**).

![Imporditud konfiguratsioonid lehel Konfiguratsioonid](./media/er-data-debugger-configurations.png)

Kui konfiguratsioonipuus puudub mõni varasemalt loetletud konfiguratsioon, siis peate need käsitsi LCS-i ühiste vahendite teegist alla laadima samal viisil, nagu laadisite alla ER-maksevormingu **ISO20022 kreeditülekanne**.

### <a name="analyze-the-downloaded-er-solution"></a>Allalaaditud ER-lahenduse analüüsimine

#### <a name="review-the-model-mapping"></a>Mudeli vastendamise läbivaatamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige **Maksemudel** \> **Maksemudeli vastendus 1611**.
3. Valige **Kujundaja**.
4. Valige vastendamiskirje **Maksemudeli vastendus ISO20022 CT**.
5. Valige **Kujundaja** ja seejärel vaadake läbi avatud mudelivastendus.

    Pange tähele, et andmemudeli väli **Maksed** on seotud andmeallikaga **\$notSentTransactions**, mis tagastab töödeldavate hankija maksete ridade loetelu.

    ![Maksete väli mudelivastendamise kujundaja lehel](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Vormingu vastendamise läbivaatamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige **Maksemudel** \> **ISO20022 kreeditülekanne**.
3. Valige **Kujundaja**.
4. Teostage lehel **Vastendamine** avatud vorminguvastenduse läbivaatus.

    Pange tähele, et faili **ISO20022CTReports** \> **XMLHeader** element **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** on seotud andmeallikaga **\$PaymentByDebtor**, mis on andmemudeli väljal **Maksed** konfigureeritud grupi kirjetesse.

    ![PmtInf element vormingukujundaja lehel](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Vormingu läbivaatamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige **Maksemudel** \> **ISO20022 kreeditülekanne**.
3. Valige **Kujundaja** ja seejärel vaadake läbi avatud vorming.

    Pange tähele, et suvandi **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** all toodud vormingu element on konfigureeritud hankija konto IBAN-koodi sisestamiseks maksefaili.

    ![BankIBAN element vormingukujundaja lehel](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>2. lisa: ostureskontro konfigureerimine

### <a name="modify-a-vendor-property"></a>Hankija atribuudi muutmine

1. Avage **Ostureskontro** \> **Hankijad** \> **Kõik hankijad**.
2. Valige hankija **DE-01002** ja seejärel valige toimingupaani vahekaardil **Hankija** grupis **Seadistamine** suvand **Pangakontod**.
3. Valige kiirkaardil **Identifitseerimine** väli **IBAN**, <a name="enteredIBANcode"></a>sisestage **GB33 BUKB 2020 1555 5555 55**.
4. Valige käsk **Salvesta**.

![IBAN-i väli hankija pangakontode lehel](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Makseviisi seadistamine

1. Avage **Ostureskontro** \> **Maksmise seadistamine** \> **Makseviisid**.
2. Valige makseviis **SEPA CT**.
3. Seadistage kiirkaardi **Failivormingud** jaotises **Failivormingud** suvandi **Üldine elektrooniline ekspordivorming** sätteks **Jah**.
4. Valige väljal **Ekspordivormingu konfiguratsioon** ER-vorming **ISO20022 kreeditülekanne**.
5. Valige käsk **Salvesta**.

![Failivormingu sätted makseviiside lehel](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Hankija makse lisamine

1. Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.
2. Lisage uus makseleht.
3. Valige **Read** ja lisage uus makserida.
4. Valige väljal **Konto** hankija **DE-01002**.
5. Sisestage väljale **Deebet** väärtus.
6. Valige väljal **Makseviis** **SEPA CT**.
7. Valige käsk **Salvesta**.

![Lisatud hankija makse hankija maksete lehel](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>3. lisa: hankija makse töötlemine

1. Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.
2. Valige lehel **Hankija maksete tööleht** varasemalt loodud maksete tööleht ja seejärel valige **Read**.
3. Valige makserida ja seejärel valige **Makse olek** \> **Puudub**.
4. Valige **Loo maksed**.
5. Valige väljal **Makseviis** **SEPA CT**.
6. Valige väljal **Pangakonto** suvand **DEMF OPER**.
7. Valige dialoogiaknas **Maksete loomine** suvand **OK**.
8. Valige dialoogiaknas **Elektroonilise aruandluse parameetrid** suvand **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]