---
title: Brasiilia elektroonilise arvelduse lisandmooduli kasutamise alustamine
description: Sellest teemast leiate teabe, mis aitab teil rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management Brasiilia elektroonilise arvelduse lisandmoodulit kasutama hakata.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0320bd1d9e93cc30ed75f28e387ac2ec8dbfc226
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962830"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Brasiilia elektroonilise arvelduse lisandmooduli kasutamise alustamine 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Brasiilia elektroonilise arvelduse lisandmoodul ei toeta praegu kõiki funktsioone, mis on saadaval finantsdokumendi integratsioonis, mis on sisse ehitatud rakendustesse Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management.

Sellest teemast leiate teabe, mis aitab teil Brasiilia elektroonilise arvelduse lisandmoodulit kasutama hakata. Selles antakse juhiseid konfiguratsioonisammude kohta, mis on riigipõhised teenustes Regulatory Configuration Services (RCS) ning rakendustes Finance ja Supply Chain Management. Samuti on selles juhised teenuse kaudu NF-e finantsdokumendi (elektroonilise finantsdokumendi mudel 55) esitamiseks ning selles selgitatakse, kuidas vaadata üle töötlemise tulemused ja finantsdokumentide olek.

## <a name="prerequisites"></a>Eeltingimused

Enne selle teema juhiste täitmist peate järgima teemas [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md) olevaid juhiseid.

## <a name="rcs-setup"></a>RCS-i seadistus

RCS-i seadistuse käigus teete järgmist.

1. E-arvelduse funktsiooni importimine NF-e finantsdokumentide jaoks.
2. Failivormingute ülevaatamine, mis on vajalikud NF-e finantsdokumentide edastamiseks autoriseerimise eesmärgil.
3. Failivormingute ülevaatamine, mis on vajalikud kinnitatud NF-e tühistamise taotlemiseks.
4. Sündmuse konfigureerimine, mis on vajalik NF-e finantsdokumentide edastamiseks autoriseerimise eesmärgil.
5. Sündmuse konfigureerimine, mis on vajalik kinnitatud NF-e tühistamise taotlemiseks.
6. E-arvelduse funktsiooni määramine elektroonilise arvelduse lisandmooduli keskkonnale.
7. E-arvelduse funktsiooni avaldamine.

> [!NOTE]
> „E-arvelduse funktsioon” on kindla ressursi üldnimi, mis on konfigureeritud ja avaldatud kasutama elektroonilise arvelduse lisandmooduli serverit. E-arvelduse funktsiooni seadistus hõlmab muu hulgas elektroonilise aruandluse (ER) konfiguratsiooni vormingute kasutamist, et luua konfigureeritavaid ekspordi- ja impordifaile, ning tegevuste ja tegevusvoogude kasutamist, et luua konfigureeritavaid reegleid taotluste saatmiseks, vastuste importimiseks ning vastuste sisu sõelumiseks.

## <a name="import-the-e-invoicing-feature"></a>E-arvelduse funktsiooni importimine

1. Logige oma RCS-i kontole sisse
2. Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** paan **E-arveldus**.
3. Valige lehel **E-arvelduse funktsioonid** suvand **Impordi**, et importida globaalsest hoidlast NF-e finantsdokumendi e-arvelduse funktsioon.

    ![Nupp „Impordi”](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Valige NF-e finantsdokumendi funktsioon ja seejärel valige **Impordi**.

    ![NF-e funktsiooni importimine](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>NF-e finantsdokumendi funktsiooni uue versiooni loomine

- Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** suvand **Uus**.

![E-arvelduse funktsiooni uue versiooni lisamine](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Konfiguratsiooni versiooni uuendamine

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Konfiguratsioonid** suvand **Lisa** või **Kustuta**, et hallata konfiguratsiooni versioone (ER-i failivormingu konfiguratsioone).

    ![E-arvelduse funktsiooni konfiguratsioonide haldamine](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - NF-e finantsdokumendi funktsiooni uue versiooni loomisel päritakse kõik konfiguratsiooniversioonid (ER-i failivormingud) uusimast versioonist.
    - NF-e finantsdokumendi edastamiseks autoriseerimise eesmärgil on vajalikud järgmised konfiguratsiooniversioonid.

        - NFe edastuse ekspordivorming
        - NFe vastuseteate importimine
        - NFe tõrkelogi importimine

    - NF-e tühistamise edastamiseks on vajalik järgmine konfiguratsiooniversioon.

        - NFe tühistamise ekspordivorming

2. Valige loendist konfiguratsiooni versioon ja seejärel suvand **Redigeeri** või **Kuva**, et avada leht **Vormingukujundaja**, kus saate konfiguratsiooni redigeerida või vaadata.

    ![Vormingukujundaja lehe avamine](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Kasutage ER-i vormingu failikonfiguratsioonide redigeerimiseks või kuvamiseks lehte **Vormingukujundaja**. Lisateavet leiate jaotisest [Elektrooniliste dokumentide konfiguratsioonide loomine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Vormingukujundaja leht](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>E-arvelduse funktsiooni seadistuste haldamine

- Valige lehel **E-arvelduse funktsioonid** vahekaardil **Seadistused** suvand **Lisa** või **Kustuta**, et hallata e-arvelduse funktsiooni seadistusi (st NF-e sündmusi).

![E-arvelduse funktsiooni seadistuste haldamine](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Kui loote NF-e finantsdokumendi funktsiooni uue versiooni, mis on tuletatud mõnest teisest e-arvelduse funktsioonist, päritakse kõik funktsiooniseadistused (NF-e sündmused) uusimast versioonist.

NF-e finantsdokumentide edastamiseks autoriseerimise eesmärgil on vajalik funktsiooniseadistus **Edastus**.

NF-e tühistamise edastamiseks on vajalik funktsiooniseadistus **Tühistamine**.

#### <a name="configure-the-submit-feature-setup"></a>Edastusfunktsiooni seadistuse konfigureerimine

1. Valige lehe **E-arvelduse funktsioonid** vahekaardi **Seadistused** veerus **Funktsiooni seadistus** suvand **Edastus**.
2. Valige suvand **Redigeeri**.

    ![E-arvelduse funktsiooni seadistuse redigeerimine](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. Valige lehel **Funktsiooni versiooni seadistus** vahekaart **Tegevused**, et hallata tegevuste loendit.

    ![Tegevuste vahekaart](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Tegevuste ülevaatamine, mis on vajalikud NF-e edastamiseks autoriseerimise eesmärgil.

    | Tegevuse ID | Tegevuse nimi                  | Tegevuse kirjeldus                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Teisenda dokument           | NF-e XML-faili loomine edastamiseks.                          |
    | 2         | Allkirjasta dokument                | Digitaalserdi lisamine XML-failile.                    |
    | 3         | Kutsu Brasiilia SEFAZ teenust | Allkirjastatud XML-fail edastamine veebiteenustele autoriseerimise eesmärgil. |
    | 4         | Töötle vastust             | Veebiteenuse vastuse hankimine.                                     |
    | 5         | Teisenda dokument           | Vastusena saadud faili sisu sõelumine.     |
    | 6         | Teisenda dokument           | XML-faili loomine edastuse oleku kohta teabe küsimiseks.    |
    | 7         | Kutsu Brasiilia SEFAZ teenust | XML-faili edastamine, mis küsib edastuse olekut.          |
    | 8         | Töötle vastust             | Veebiteenuse vastuse hankimine.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>SEFAZ veebiteenuste URL-i seadistamine 

1. Valige lehel **Funktsiooni versiooni seadistus** vahekaardi **Tegevused** kiirkaardilt **Tegevused** suvand **Kutsu Brasiilia SEFAZ teenust** (tegevuse ID **3**).
2. Sisestage kiirkaardil **Parameetrid** väljale **URL-aadressi parameeter** NF-e edastamiseks SEFAZ veebiteenuse URL.
3. Valige kiirkaardil **Tegevused** suvand **Kutsu Brasiilia SEFAZ teenust** (tegevuse ID **7**).
4. Sisestage kiirkaardil **Parameetrid** väljale **URL-aadressi parameeter** NF-e edastamiseks SEFAZ veebiteenuse URL.

#### <a name="configure-the-cancellation-feature-setup"></a>Tühistamisfunktsiooni seadistuse konfigureerimine

1. Valige lehe **E-arvelduse funktsioonid** vahekaardi **Seadistused** veerus **Funktsiooni seadistus** suvand **Tühistamine**.
2. Valige suvand **Redigeeri**.
3. Valige lehel **Funktsiooni versiooni seadistus** vahekaart **Tegevused**, et hallata tegevuste loendit.
4. Vaadake üle tegevused, mis on vajalikud kinnitatud NF-e tühistamise taotlemiseks.

    | Tegevuse ID | Tegevuse nimi                  | Tegevuse kirjeldus                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Teisenda dokument           | NF-e tühistamise XML-faili loomine edastamiseks.            |
    | 2         | Allkirjasta dokument                | Digitaalserdi lisamine XML-failile.                   |
    | 3         | Kutsu Brasiilia SEFAZ teenust | Allkirjastatud XML-fail edastamine veebiteenustele tühistamise eesmärgil. |
    | 4         | Töötle vastust             | Veebiteenuse vastuse hankimine.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>SEFAZ veebiteenuste URL-i seadistamine

1. Valige lehel **Funktsiooni versiooni seadistus** vahekaardi **Tegevused** kiirkaardilt **Tegevused** suvand **Kutsu Brasiilia SEFAZ teenust** (tegevuse ID **3**).
2. Sisestage kiirkaardil **Parameetrid** väljale **URL-aadressi parameeter** kinnitatud NF-e tühistamiseks SEFAZ veebiteenuse URL.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>E-arvelduse keskkonna kättesaadavaks tegemine ja mustandversiooni määramine

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Keskkonnad** suvand **Luba**.
2. Valige keskkond väljal **Keskkond**.
3. Valige väljal **Kehtiv alates** kuupäev, mil uus keskkond peaks kehtima hakkama.
4. Valige **Luba**.

![E-arvelduse keskkonna lubamine](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Oleku muutmine lõpetatuks

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Mustand**.
2. Valige **Muuda olekut \> Lõpule viidud**.

### <a name="change-the-status-to-publish"></a>Oleku muutmine avaldatuks

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Lõpetatud**.
2. Valige **Muuda olekut \> Avalda**.

![E-arvelduse funktsiooni avaldamine](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Elektroonilise arvelduse lisandmooduli integratsiooni seadistamine rakenduses Finance või Supply Chain Management

Seadistuse käigus teete järgmist.

1. Brasiilia NF-e föderaalse funktsiooni sisselülitamine.
2. Kindla ER-i andmemudeli, ER-i andmemudeli vastenduse ja NF-e finantsdokumentide jaoks vajalike vormingute importimine.
3. ER-i konfiguratsiooni importimine ja vastusetüüpide seadistamine, mis on vajalikud finantsdokumendi oleku värskendamiseks pärast edastusprotsessi tagastamist.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Brasiilia NF-e föderaalse funktsiooni sisselülitamine

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Märkige vahekaardil **Funktsioonid** märkeruut **Luba** funktsiooniviite **BR00053** rea puhul.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>NF-e finantsdokumentide jaoks vajaliku ER-i andmemudeli vastenduse importimine

1. Logige sisse rakendusse Finance.
2. Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** paan **Microsoft**. Veenduge, et konfiguratsioonipakkuja olekuks oleks seatud **Aktiivne**. Lisateavet pakkuja **aktiivseks** märkimise kohta leiate teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Valige **Osad**.
4. Valige **Globaalne ressurss \> Ava**.
5. Importige **Finantsdokumentide vastenduse** konfiguratsioonid.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>ER-i konfiguratsioonide importimine ja vastusetüüpide seadistamine finantsdokumentide jaoks

1. Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** paan **Microsoft**.
2. Valige **Osad**.
3. Valige **Globaalne ressurss \> Ava**.
4. Importige **NF-e tõrkelogi importimine (BR)**, **NF-e vastuseandmete impordivorming (BR)** ja **NF-e vastuseteate importimine (BR)**.
5. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
6. Valige lehel **Elektrooniline dokument** suvand **Lisa**.
6. Sisestage väljale **Tabeli nimi** tekst **Finantsdokumendi päis**.
7. Valige väljal **Dokumendi kontekst** suvand **Kliendiarve kontekstimudel – finantsdokumendi kontekst**.
8. Valige **Vastusetüübid**.
9. Valige **Uus** ja valige siis väljal **Vastusetüüp** suvand **Vastus**.
10. Valige väljal **Edastuse olek** suvand **Ootel**.
11. Valige väljal **Mudelivastendus** suvand **Vastuseteate impordivorming – mudelivastendus vastuseteatest**.
12. Valige käsk **Salvesta**.
13. Valige **Uus** ja sisestage siis väljale **Vastusetüüp** väärtus **ResponseData**.
14. Valige väljal **Edastuse olek** suvand **Ootel**.
15. Valige väljal **Mudelivastendus** suvand **NFe vastuseandmete impordivorming – vastuseandmete importimine**.
16. Valige käsk **Salvesta**.

## <a name="electronic-invoice-processing"></a>Elektroonilise arve töötlemine

Rakenduses Finance teete töötlemise käigus järgmist.

1. Finantsdokumendi edastamine elektroonilise arvelduse lisandmooduli kaudu.
2. Edastuse käivituslogide vaatamine ja töötlemise tulemuste ülevaatamine.
3. Finantsdokumendi tühistamise edastamine elektroonilise arvelduse lisandmooduli kaudu.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>NF-e finantsdokumentide edastamine SEFAZ-is autoriseerimiseks 

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist pole enam võimalik kasutada vana protsessi NF-e finantsdokumentide edastamiseks autoriseerimise eesmärgil (**NF-e eksportimise/importimise protsess**). See asendatakse uue protsessiga **Edasta elektroonilised dokumendid**.

> [!NOTE]
> Enne jätkamist veenduge, et teil on üks või mitu kliendi finantsdokumentide mudelit 55, mille väljastas kliendi finantsasutus. Nende finantsdokumentide suunaks peab olema määratud **Väljuv** ja olekuks **Loodud**. Lisateavet leiate teemast [Kliendi finantsdokumendi väljastamine (Brasiilia)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Edasta elektroonilised dokumendid**.
2. Mis tahes dokumendi esimese edastamise korral seadke suvandi **Dokumentide taasedastamine** väärtuseks alati **Ei**. Kui peate dokumendi teenuse kaudu uuesti edastama, seadke selle suvandi väärtuseks **Jah**.
3. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**, et avada dialoogiboks **Päring**, kus saate luua päringu edastatavate dokumentide valimiseks.
4. Valige vahekaardil **Vahemik** suvand **Lisa**.
5. Valige väljal **Tabel** suvand **Finantsdokumendi päis**.
6. Valige väljal **Tuletatud tabel** suvand **Finantsdokumendi päis**.
6. Valige väljal **Väli** suvand **Arv**.
7. Sisestage väljale **Kriteerium** edastatavate finantsdokumentide arv.
8. Valige dialoogiboksi **Päring** sulgemiseks **OK**.
8. Valige **OK**, et valitud dokumendid edastada.

> [!NOTE]
> Esimesel dokumendi edastamise katsel teenuse kaudu palutakse teil kinnitada ühendus elektroonilise arvelduse lisandmooduliga. Valige **Elektroonilise dokumendi edastusteenusega ühendumiseks klõpsake siin**.

### <a name="view-all-submission-logs"></a>Kõigi edastuslogide kuvamine

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist on saadaval uus leht, mis võimaldab teil jälgida dokumendi edastamise edenemist. Selle lehe abil saate vaadata kõigi edastatud dokumentide edastuslogisid.

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.
2. Valige väljal **Dokumenditüüp** suvand **Finantsdokumendi päis**, et kuvada ainult finantsdokumendid.
3. Valige toimingupaanil **Päringud \> Edastuse üksikasjad**, et vaadata edastuse käivituslogide üksikasju.

![Edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> NF-e finantsdokumentide puhul on veerus **Tõrkekood** toodud tagastuskood, mille tagastasid SEFAZ veebiteenused.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Edastuslogide kuvamine finantsdokumendi lehe kaudu

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist saate vaadata edastuslogisid ka finantsdokumendi lehe kaudu.

1. Avage **Pearaamat \> Päringud ja aruanded \> Finantsdokumendid \> Kõik finantsdokumendid**.
2. Valige finantsdokument, mis esitati varem elektroonilise arvelduse lisandmooduli kaudu.
3. Valige toimingupaanil vahekaardil **NF-e federal** suvand **Elektroonilise dokumendi logi**.

![Edastuslogide kuvamine finantsdokumendi lehel](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Kinnitatud NF-e finantsdokumentide edastamine SEFAZ-is tühistamiseks

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist ei saa enam vana NF-e finantsdokumentide tühistamise protsessi kasutada. See asendatakse uue tühistamisprotsessiga, mis on manustatud lehel **Elektroonilise dokumendi edastuslogi**.

> [!NOTE]
> Veenduge, et oleksite käivitanud kinnitatud NF-e finantsdokumendi puhul kliendi finantsdokumendi tühistamise. Lisateavet leiate teemast [Kliendi finantsdokumendi tühistamine (Brasiilia)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.
2. Valige finantsdokument ja seejärel **Funktsioonid \> Saada seotud edastused**.
3. Sisestage seotud edastuse kirjeldus ja seejärel valige **OK**.

### <a name="view-cancellation-submission-logs"></a>Tühistamise edastuslogide kuvamine

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.
2. Valige väljal **Dokumenditüüp** suvand **Finantsdokumendi päis**, et kuvada ainult finantsdokumendid.
3. Valige finantsdokument ja seejärel valige toimingupaanil **Päringud \> Seotud edastus**.

    Seotud edastused on edastused, mis on seotud esimesena tehtud põhiedastusega. Näiteks on põhiedastus see edastus, mis autoriseerib kindlat NF-e finantsdokumenti. Edastus, mis taotleb sama NF-e tühistamist SEFAZ-is, on seotud edastus. See on olemas ainult seetõttu, et selle kaudu taotletakse teise edastuse kaudu tehtud töö tühistamist.

    Lehel **Seotud edastused** kuvatakse kõik asjaomase finantsdokumendiga seotud edastused ja nende edastamise olek. Järgmisel illustratsioonil tähistab esimene rida edastust, mis taotles finantsdokumendi kinnitust. Teine rida tähistab edastust, mis tühistas selle finantsdokumendi.

    ![Tühistamise edastuslogide vaatamine](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Valige toimingupaanil **Päringud \> Edastuse üksikasjad**, et vaadata edastuse käivituslogide üksikasju.

    ![Tühistamise edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Privaatsusavaldus
Funktsiooni BR-00053 (NF-e Federal) lubamise korral on võimalik, et saata tuleb piiratud andmeid, sealhulgas organisatsiooni maksukohustuslasena registreerimise ID. See edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata maksuametile elektroonilisi arveid eelmääratletud vormingus, mis on vajalik integratsiooniks valitsuse veebiteenusega. Administraator saab lubada ja keelata funktsiooni BR-00053 (NF-e Federal), avades **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**. Valige vahekaart **Funktsioonid**, valige rida, mis sisaldab funktsiooni BR-00053, ning seejärel tehke sobiv valik. Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.


## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse lisandmooduli ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md)
- [Elektroonilise arvelduse lisandmooduli seadistamine](e-invoicing-setup.md)
