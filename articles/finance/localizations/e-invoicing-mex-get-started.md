---
title: Mehhiko elektroonilise arvelduse lisandmooduli kasutamise alustamine
description: Sellest teemast leiate teabe, mis aitab teil rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management Mehhiko elektroonilise arvelduse lisandmoodulit kasutama hakata.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d719c3ba68458130d415c50319fdcdeafcfc783e
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835939"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a>Mehhiko elektroonilise arvelduse lisandmooduli kasutamise alustamine

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Elektroonilise arvelduse lisandmoodul Mehhiko jaoks ei pruugi praegu toetada kõiki funktsioone, mis on saadaval dokumendis Comprobante Fiscal Digital por Internet (CFDI) ja seotud integratsioonis, mis on sisse ehitatud rakendusse Microsoft Dynamics 365 Finance või Dynamics 365 Supply Chain Management.

Sellest teemast leiate teabe, mis aitab teil Mehhiko elektroonilise arvelduse lisandmoodulit kasutama hakata. Selles antakse juhiseid konfiguratsioonisammude kohta, mis on teenustes Regulatory Configuration Services (RCS) ja rakenduses Finance riigipõhised. Samuti antakse teile juhised, mida peate rakenduses Finance järgima, et edastada teenuse kaudu CFDI arveid, ning selgitatakse, kuidas vaadata üle töötlemise tulemusi ja CFDI arvete olekut.

## <a name="prerequisites"></a>Eeltingimused

Enne selle teema juhiste täitmist peate järgima teemas [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md) olevaid juhiseid.

## <a name="rcs-setup"></a>RCS-i seadistus

RCS-i seadistuse käigus teete järgmist.

1. E-arvelduse funktsiooni importimine CFDI arvete töötlemiseks.
2. Vormingu konfiguratsioonide ülevaatamine, mis on vajalikud CFDI arvete loomiseks, edastamiseks ja nende vastuste vastu võtmiseks ning tühistamisega seotud vastuste edastamiseks ja vastu võtmiseks.
3. CFDI arve edastamise stsenaariume toetavate sündmuste konfigureerimine.
4. E-arvelduse funktsiooni avaldamine CFDI arvete jaoks.

> [!NOTE]
> „E-arvelduse funktsioon” on kindla ressursi üldnimi, mis on konfigureeritud ja avaldatud kasutama elektroonilise arvelduse lisandmooduli serverit. Praegusel juhul on seadistatavaks e-arvelduse funktsiooniks CFDI arved (MX).

## <a name="import-the-e-invoicing-feature"></a>E-arvelduse funktsiooni importimine

1. Logige oma RCS-i kontole sisse.
2. Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** paan **E-arveldus**.
3. Valige lehel **E-arvelduse funktsioonid** suvand **Impordi**, et importida globaalsest hoidlast funktsioon **CFDI arved (MX)**.

    > [!NOTE]
    > Kui te funktsiooni loendis ei näe, valige **Sünkrooni** ja seejärel korrake kolmandat sammu.

![CFDI arvete (MX) funktsiooni importimine](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Funktsiooni **CFDI arved (MX)** importimisel globaalsest hoidlast imporditakse ka kõik funktsiooni sätted, sealhulgas konfiguratsioonid ja tegevused.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>CFDI arvete (MX) funktsiooni uue versiooni loomine

Saate luua uue versiooni, kui URL-i on näiteks vaja värskendada. Lisateavet leiate teemast [E-arvelduse CFDI](tasks/mx-00010-e-invoicing-cfdi.md).

- Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** suvand **Uus**.

![E-arvelduse funktsiooni uue versiooni lisamine](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Konfiguratsiooni versiooni uuendamine

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Konfiguratsioonid** suvand **Lisa** või **Kustuta**, et hallata konfiguratsiooni versioone (ER-i failivormingu konfiguratsioone).

    ![E-arvelduse funktsiooni konfiguratsioonide haldamine](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Uue versiooni loomisel päritakse kõik konfiguratsioonid viimasest avaldatud versioonist. CFDI arvete töötlemiseks on vajalikud järgmised konfiguratsioonid.

    - CFDI arve (BusinessDocumentService)
    - CFDI vastuseteate importimine
    - CFDI tõrkelogi importimine
    - CFDI tühistamistaotlus (MX) (BusinessDocumentService)
    - CFDI arve (BusinessDocumentService)

2. Valige loendist konfiguratsiooni versioon ja seejärel suvand **Redigeeri** või **Kuva**, et avada leht **Vormingukujundaja**, kus saate konfiguratsiooni redigeerida või vaadata.

    ![Vormingukujundaja lehe avamine](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Kasutage ER-i vormingu failikonfiguratsioonide redigeerimiseks ja kuvamiseks lehte **Vormingukujundaja**. Lisateavet leiate jaotisest [Elektrooniliste dokumentide konfiguratsioonide loomine](../../dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Vormingukujundaja leht](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>E-arvelduse funktsiooni seadistuste haldamine

- Valige lehel **E-arvelduse funktsioonid** vahekaardil **Seadistused** suvand **Lisa**, **Kustuta** või **Redigeeri**, et hallata e-arvelduse funktsiooni seadistusi.

![E-arvelduse funktsiooni seadistuste haldamine](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

CFDI arvete edastamiseks autoriseerimise eesmärgil (XML-faili loomiseks, XML-faili edastamiseks ja vastuse töötlemiseks) on vajalik funktsiooniseadistus **Müügiarve**.

CFDI arve tühistamise edastamiseks on vajalikud funktsiooniseadistused **Tühistamine** ja **Tühista**.

### <a name="configure-the-sales-invoice-feature-setup"></a>Müügiarve funktsiooni seadistuse konfigureerimine

1. Valige lehe **E-arvelduse funktsioonid** vahekaardi **Seadistused** veerus **Funktsiooni seadistus** suvand **Müügiarve**.
2. Valige **Redigeeri**, et konfigureerida tegevused, rakendatavuse reeglid ja muutujad.

    ![E-arvelduse funktsiooni seadistuse redigeerimine](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. Valige lehel **Funktsiooni versiooni seadistus** vahekaart **Tegevused**, et hallata tegevuste loendit. Tegevused määratlevad selliste toimingute loendi, mis tuleb käitada sündmuse täielikuks lõpetamiseks järjestikku.

    ![Tegevuste vahekaart](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Tegevuse ID | Tegevus                   | Tegevuse nimi                                  | Tegevuse kirjeldus                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Teisenda dokument       | Loo CFDI e-arve digitaalallkirjata | CFDI e-arve loomine.                                |
    | 2         | Allkirjasta dokument            | Digitaalallkiri                                 | E-arve digitaalne allkirjastamine edastamiseks.                |
    | 3         | Kutsu Mehhiko PAC teenust | Edasta CFDI e-arve                        | Windows Communication Foundationi (WCF) klient edastab CFDI e-arve. |
    | 4         | Töötle vastust         | Analüüsi veebiteenuse vastust                 | Veebiteenuse vastuse analüüsimine ja tõrkelogi tagastamine. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Mehhiko PAC veebiteenuste URL-i seadistamine 

1. Valige lehel **Funktsiooni versiooni seadistus** vahekaardi **Tegevused** kiirkaardilt **Tegevused** suvand **Kutsu Mehhiko PAC teenust**.
2. Sisestage kiirkaardil **Parameetrid** väljale **URL-aadress** CFDI arve edastamiseks veebiteenuse URL.

> [!NOTE]
> Kasutage samu samme, et värskendada tegevuse **Kutsu Mehhiko PAC teenust** URL-i funktsiooniseadistuste **Tühista** ja **Tühistamistaotlus** jaoks.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Mustandversiooni määramine e-arvelduse keskkonnale

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Keskkonnad** suvand **Luba**.
2. Valige keskkond väljal **Keskkond**.
3. Valige väljal **Kehtiv alates** kuupäev, mil uus keskkond peaks kehtima hakkama.
3. Valige **Luba**.

![E-arvelduse keskkonna lubamine](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Versiooni oleku muutmine lõpetatuks

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Mustand**.
2. Valige **Muuda olekut \> Lõpule viidud**.

## <a name="change-the-version-status-to-published"></a>Versiooni oleku muutmine avaldatuks

- Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** suvand **Muuda olekut \> Avalda**.

## <a name="publish-the-e-invoicing-feature"></a>E-arvelduse funktsiooni avaldamine

1. Valige lehel **E-arvelduse funktsioonid** vahekaart **Versioonid**, et hallata funktsiooni **CFDI arved (MX)** olekut.
2. Valige **Muuda olekut**, et muuta funktsiooni olekut.

![E-arvelduse funktsiooni oleku muutmine](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a>Elektroonilise arvelduse lisandmooduli integratsiooni seadistamine rakenduses Finance

Elektroonilise arvelduse lisandmooduli seadistamise käigus rakenduses Finance teete järgmist.

1. ER-i andmemudeli, ER-i andmemudeli vastenduse ja CFDI arvete jaoks vajalike vormingute importimine.
2. Vastusetüüpide konfigureerimine CFDI arvete värskendamiseks. Vastusetüüpe kasutatakse autoriseeritud serdipakkuja (PAC) serveri vastuse jaoks.

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>ER-i andmemudeli, ER-i andmemudeli vastenduse ja CFDI arvete kontekstikonfiguratsioonide importimine

1. Logige sisse rakendusse Finance.
2. Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** pealkiri **Microsoft**. Veenduge, et konfiguratsioonipakkuja olekuks oleks seatud **Aktiivne**. Lisateavet pakkuja **aktiivseks** märkimise kohta leiate teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Valige **Osad**.
4. Valige **Globaalne ressurss \> Ava**.
5. Importige **Arvemudel**, **Arvemudeli vastendus**, **CFDI arve vorming (MX)**, **CFDI arve tühistamistaotluse vorming (MX)** ja **CFDI arve tühistamisvorming (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>Funktsiooni sisselülitamine CFDI arvete töötlemiseks

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Märkige vahekaardil **Funktsioonid** märkeruut **Luba** funktsiooniviidete **MX-00010** ja **MX-00016** ridade puhul.

![Funktsioonide sisselülitamine CFDI arvete töötlemiseks](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>ER-i konfiguratsioonide importimine ja vastusetüüpide seadistamine CFDI arvete värskendamiseks

#### <a name="import-er-configurations"></a>Elektroonilise aruandluse konfiguratsioonide importimine

1. Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** pealkiri **Microsoft**.
3. Valige **Osad**.
4. Valige **Globaalne ressurss \> Ava**.
5. Importige **Vastuseteate mudel**, **CFDI tõrkelogi importimine (MX)**, **CFDI tõrkelogi importimine (MX)** ja **CFDI vastuseteate importimine (MX)**.

#### <a name="set-up-the-response-types"></a>Vastusetüüpide seadistamine

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Valige lehel **Elektrooniline dokument** suvand **Lisa**.
3. Sisestage kliendiarve tööleht ja seejärel valige väljal **Tabeli nimi** projektiarve.
4. Määratlege iga tabeli puhul seotud dokumendi kontekst.

    - Sisestage suvandi **Kliendiarve tööleht** puhul **Kliendiarve kontekst**.
    - Sisestage suvandi **Projektiarve** puhul **Projektiarve kontekst**.

4. Valige **Vastusetüübid**, et konfigureerida vastusetüübid, mida saab elektroonilise arvelduse lisandmoodulist tagastada ja lisada kliendiarve töölehele või projektiarvele.
5. Valige **Uus** ja valige siis väljal **Vastusetüüp** suvand **Vastus**.
6. Valige väljal **Edastuse olek** suvand **Ootel**.
7. Valige väljal **Mudelivastendus** suvand **Vastuseteate impordivorming – mudelivastendus vastuseteatest**.
8. Valige käsk **Salvesta**.
9. Valige **Uus** ja valige siis väljal **Vastusetüüp** suvand **ResponseData**.
10. Valige väljal **Edastuse olek** suvand **Ootel**.
11. Valige väljal **Mudelivastendus** suvand **CFDI vastuseandmete impordivorming (üksikasjad) – vastuseandmete importimine**.
12. Valige käsk **Salvesta**.

## <a name="process-electronic-invoices-in-finance"></a>Elektrooniliste arvete töötlemine rakenduses Finance 

CFDI arvete töötlemisel rakenduses Finance elektroonilise arvelduse lisandmooduli kaudu saate teha järgmisi toiminguid.

- CFDI arvete edastamine.
- Edastuse käivituslogide kuvamine.
- CFDI arve tühistamise edastamine.

### <a name="submit-cfdi-invoices"></a>CFDI arvete edastamine

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist pole CFDI arvete edastamiseks enam võimalik kasutada protsessi **Ekspordi/impordi elektrooniline arve** (**Müügireskontro \> Arved \> E-arved**). See asendatakse uue protsessiga **Edasta elektroonilised dokumendid**.

> [!NOTE]
> Enne uue protsessi **Edasta elektroonilised dokumendid** kasutamist veenduge, et Mehhiko e-arvete jaoks vajalik seadistus oleks lõpetatud. Lisateavet leiate teemast [CFDI paigutuse versioon 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Edasta elektroonilised dokumendid**.
2. Mis tahes dokumendi esimese edastamise korral seadke suvandi **Dokumentide taasedastamine** väärtuseks alati **Ei**. Kui peate dokumendi teenuse kaudu uuesti edastama, seadke selle suvandi väärtuseks **Jah**.
3. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**, et avada dialoogiboks **Päring**, kus saate luua päringu edastatavate dokumentide valimiseks.

![CFDI dokumendi edastamine](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Esimesel dokumendi edastamise katsel teenuse kaudu palutakse teil kinnitada ühendus elektroonilise arvelduse lisandmooduliga. Valige **Elektroonilise dokumendi edastusteenusega ühendumiseks klõpsake siin**.

### <a name="view-submission-logs"></a>Edastuslogide kuvamine

Saate vaadata kõigi edastatud dokumentide või ainult ühe edastatud dokumendi edastuslogisid.

#### <a name="view-all-submission-logs"></a>Kõigi edastuslogide kuvamine

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist on saadaval uus leht, mis võimaldab teil jälgida dokumendi edastamise edenemist. Selle lehe abil saate vaadata kõigi edastatud dokumentide edastuslogisid.

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.
2. Valige väljal **Dokumenditüüp** suvand **Kliendiarve tööleht**, et kuvada vajalikud elektroonilised dokumendid.

    ![Dokumendi tüübi valimine edastuslogide kuvamiseks](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Valige toimingupaanil **Päringud \> Edastuse üksikasjad**, et vaadata edastuse käivituslogide üksikasju.

    ![Edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Edastuslogide teave on jagatud kolme kiirkaardi vahel.

- **Töötlemistegevused** – sellel kiirkaardil näidatakse RCS-is seadistatud funktsiooni versioonis konfigureeritud tegevuste käivituslogi. Veerus **Olek** on näha, kas tegevuse käivitamine õnnestus.
- **Tegevusfailid** – sellel kiirkaadil on vahefailid, mis loodi tegevuste käivitamise ajal. Saate valida **Kuva**, et fail alla laadida ja seda vaadata.
- **Töötlemise tegevuslogi** – sellel kiirkaardil on kuvatud elektroonilise arvelduse lisandmooduli ja sihtveebiteenuse vahelise suhtluse tulemused. See näitab ka, mis tagastati veebiteenuse töötlemise käigus. Veerus **Tõrkekood** on toodud tagastuskood, mis tagastati autoriseerivast veebiteenusest.

Kui edastatud CFDI arve on autoriseeritud, määratakse selle olekuks väärtus **Kinnitatud**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Edastuslogide kuvamine CFDI arvetes

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist saate vaadata edastuslogisid ka CFDI arvetes.

1. Avage **Müügireskontro \> Päringud ja aruanded \> CFDI (elektroonilised arved)**.
2. Valige CFDI arve, mis edastati pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist.
3. Valige toimingupaanil vahekaardil **Ajalugu** suvand **Elektroonilise dokumendi logi**.

![Edastuslogide vaatamine CFDI arvetes](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> CFDI arvete puhul, mis edastati enne funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist, on saadaval nupp **Ajalugu**. CFDI arvete puhul, mis edastati pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist, pole nupp **Ajalugu** saadaval.

### <a name="submit-cancellation-of-cfdi-invoices"></a>CFDI arvete tühistamise edastamine

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist ei saa enam vana CFDI arvete tühistamise protsessi kasutada. See asendatakse uue tühistamisprotsessiga, mis on manustatud lehel **Elektroonilise dokumendi edastuslogi**.

1. Avage **Müügireskontro \> Päringud ja aruanded \> CFDI (elektroonilised arved)**.
2. Kui CFDI arve olek on **Kinnitatud**, valige **Funktsioonid \> Tühista CFDI**.
3. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.
4. Valige CFDI arve ja seejärel **Funktsioonid \> Saada seotud edastused**.
5. Sisestage seotud edastuse kirjeldus ja seejärel valige **OK**.

#### <a name="view-cancellation-submission-logs"></a>Tühistamise edastuslogide kuvamine

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.
2. Valige väljal **Dokumenditüüp** suvand **Kliendiarve tööleht**, et kuvada ainult kliendiarve töölehe dokumendid.
3. Valige CFDI arve ja seejärel valige toimingupaanil **Päringud \> Seotud edastus**.

    Lehel **Seotud edastused** kuvatakse kõik asjaomase CFDI arvega seotud edastused ja nende edastamise olek. Järgmisel illustratsioonil tähistab esimene rida edastust, mis taotles CFDI arve kinnitust. Teine rida tähistab edastust, mis tühistas selle CFDI arve.

    ![Tühistamise edastuslogide vaatamine](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Valige toimingupaanil **Päringud \> Edastuse üksikasjad**, et vaadata edastuse käivituslogide üksikasju.

    ![Tühistamise edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Privaatsusavaldus
Funktsioonide MX-00010 ja MX-00016 (CFDI arve ja CFDI tühistamine) lubamise korral on võimalik, et saata tuleb piiratud andmeid, sealhulgas organisatsiooni maksukohustuslasena registreerimise ID. See edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata maksuametile elektroonilisi arveid eelmääratletud vormingus, mis on vajalik integratsiooniks valitsuse veebiteenusega. Administraator saab lubada ja keelata funktsioonid MX-00010 ja MX-00016 (CFDI arve ja CFDI tühistamine), avades **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**. Valige vahekaart **Funktsioonid**, valige read, mis sisaldavad funktsioone MX-00010 ja MX-00016, ning seejärel tehke sobiv valik. Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse lisandmooduli ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md)
- [Elektroonilise arvelduse lisandmooduli seadistamine](e-invoicing-setup.md)