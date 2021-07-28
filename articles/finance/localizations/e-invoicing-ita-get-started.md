---
title: Elektroonilise arvelduse lisandmooduli kasutamise alustamine Itaalias
description: Sellest teemast leiate teabe, mis aitab teil alustada elektroonilise arveldusega Itaalias.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 8bbb78f0b20ec12fe59dfb3c656b3177b2464004
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356073"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a>Elektroonilise arvelduse lisandmooduli kasutamise alustamine Itaalias

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Itaalia elektroonilise arvelduse lisandmoodul ei pruugi praegu toetada kõiki elektrooniliste arvete jaoks saadaolevaid funktsioone rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management. 

Sellest teemast leiate teabe, mis aitab teil alustada elektroonilise arveldusega Itaalias. Selles antakse juhiseid konfiguratsioonisammude kohta, mis on teenustes Regulatory Configuration Services (RCS) ja rakenduses Finance riigipõhised. Samuti antakse juhiseid selle kohta, kuidas edastada teenuse kaudu elektroonilisi arveid, mis on loodud Itaalia-põhises vormingus **FatturaPA**, ja selgitatakse, kuidas töötlemise tulemusi üle vaadata.

## <a name="prerequisites"></a>Eeltingimused

Enne selle teema juhiste täitmist peate järgima teemas [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md) olevaid juhiseid.

## <a name="rcs-setup"></a>RCS häälestus

RCS-i seadistuse käigus teete järgmist.

1. E-arvelduse funktsiooni importimine kliendi elektrooniliste arvete eksportimiseks vormingus **FatturaPA**.
2. Elektrooniliste arvete loomiseks, edastamiseks ja nende vastuste vastu võtmiseks vajalike vormingukonfiguratsioonide ülevaatamine.
3. Elektroonilise arve edastamise stsenaariume toetavate sündmuste konfigureerimine.
4. E-arvelduse funktsiooni avaldamine.

> [!NOTE]
> „E-arvelduse funktsioon” on kindla ressursi üldnimi, mis on konfigureeritud ja avaldatud kasutama elektroonilise arvelduse lisandmooduli serverit. Praegusel juhul on seadistatavaks e-arvelduse funktsiooniks klientide elektrooniliste arvete eksportimine.

## <a name="import-the-e-invoicing-feature"></a>E-arvelduse funktsiooni importimine

1. Logige oma RCS-i kontole sisse.
2. Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** paan **E-arveldus**.
3. Valige lehel **E-arvelduse funktsioonid** suvand **Impordi**, et importida globaalsest hoidlast e-arvelduse funktsioon.

    > [!NOTE]
    > Kui te ei näe saadaolevate funktsioonide loendit, valige **Sünkrooni**. 

4. Valige funktsioon **E-arvete eksportimine (IT)** ja seejärel valige **Impordi**.

![E-arvete eksportimise (IT) funktsiooni importimine.](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Funktsiooni **E-arvete eksportimine (IT)** importimisel globaalsest hoidlast, imporditakse ka kõik järgmistes jaotistes kirjeldatud sätted.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>E-arvete eksportimise (IT) funktsiooni uue versiooni loomine

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** suvand **Uus**. 

    ![E-arvelduse funktsiooni uue versiooni lisamine.](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Järgmisena konfigureerite elektroonilise aruandluse (ER) vormingud, mis on e-arvelduse funktsiooniga seotud.

2. Valige vahekaardil **Konfiguratsioonid** suvand **Lisa**, et hallata konfiguratsiooni versioone.

    ![E-arvelduse funktsiooni konfiguratsiooni versioonide haldamine.](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    Selles sammus lisate ja konfigureerite ER-i vormingud eri failide jaoks, mida kasutatakse Itaalia e-arvete eksportimiseks. Itaalia FatturaPA e-arvete puhul kasutage järgmisi standardseid konfiguratsioone või tegelikke e-arvelduse jaoks kasutatavaid kohandatud konfiguratsioone.

    - Müügiarve (IT)
    - Projektiarve (IT)

    Kui loote e-arvelduse funktsiooni, mis on tuletatud mõnest muust e-arvelduse funktsioonist, päritakse kõik ER-i vormingud algsest funktsioonist.

3. Valige konkreetne ER-i vormingu failikonfiguratsioon.
4. Valige **Redigeeri** või **Kuva**, et avada leht **Vormingukujundaja**.

    ![Vormingukujundaja lehe avamine.](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Kasutage ER-i vormingu failikonfiguratsioonide redigeerimiseks ja kuvamiseks lehte **Vormingukujundaja**.

    ![Vormingukujundaja leht.](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>E-arvelduse funktsiooni seadistuste haldamine

- Valige lehel **E-arvelduse funktsioonid** vahekaardil **Seadistused** suvand **Lisa**, **Kustuta** või **Redigeeri**, et hallata e-arvelduse funktsiooni seadistusi.

![E-arvelduse funktsiooni seadistuste haldamine.](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

Selles sammus konfigureerite sündmused, mida rakendatakse elektrooniliste arvete puhul, sh XML-väljundfailide loomine vormingus **FatturaPA** ja digitaalne allkirjastamine (kui see on vajalik).

### <a name="configure-the-sales-invoice-feature-setup"></a>Müügiarve funktsiooni seadistuse konfigureerimine

1. Valige lehe **E-arvelduse funktsioonid** vahekaardi **Seadistused** veerus **Funktsiooni seadistus** suvand **Müügiarve**.
2. Valige suvand **Redigeeri**.
3. Valige lehel **Funktsiooni versiooni seadistus** vahekaart **Tegevused**, et hallata tegevuste loendit. Tegevused määratlevad selliste toimingute loendi, mis tuleb käitada sündmuse täielikuks lõpetamiseks järjestikku.

    ![Tegevuste vahekaart.](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Tegevuse ID | Tegevuse nimi        | Tegevuse kirjeldus                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Dokumendi teisendamine | E-arve XML-faili loomine vormingus **FatturaPA**. |
    | 2         | Allkirjasta dokument      | Digitaalallkirja lisamine XML-failile.             |

4. Valige vahekaart **Rakendatavuse reeglid**, et vaadata ja hallata rakendatavuse reegleid. Rakendatavuse reeglid määratlevad konteksti, mille puhul tegevus käivitatakse.

    ![Rakendatavuse reeglite vahekaart.](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Valige vahekaart **Muutujad**, et vaadata ja hallata muutujaid.

    ![Muutujate vahekaart.](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Määratlege avalikud muutujad, mis on vajalikud tegevuste käivitamiseks.

### <a name="configure-the-project-invoice-feature-setup"></a>Projektiarve funktsiooni seadistuse konfigureerimine 

Funktsiooni **Projektiarve** seadistuse konfigureerimiseks vajalikud juhised ja sätted on väga sarnased funktsiooni **Müügiarve** seadistuse juhiste ning sätetega. Projektiarvetega töötamise korral vaadake juhiseid müügiarvete kohta.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>E-arvelduse funktsiooni määramine keskkonnale

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Keskkonnad** suvand **Luba**.
2. Valige keskkond väljal **Keskkond**.
3. Valige väljal **Kehtiv alates** kuupäev, mil uus keskkond peaks kehtima hakkama.
4. Valige **Luba**. 

![E-arvelduse keskkonna lubamine.](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>E-arvelduse funktsiooni avaldamine

Saate avaldada e-arvelduse funktsiooni, muutes versiooni olekuks väärtuse **Lõpetatud** või **Avaldatud**.

### <a name="change-the-version-status-to-completed"></a>Versiooni oleku muutmine lõpetatuks

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Mustand**.
2. Valige **Muuda olekut \> Lõpule viidud**. 

### <a name="change-the-version-status-to-published"></a>Versiooni oleku muutmine avaldatuks 

1. Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Lõpetatud**.
2. Valige **Muuda olekut \> Avalda**.

![E-arvelduse funktsiooni oleku muutmine.](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a>Seadista Elektroonilise arveldamise integratsioon Finantsis

Rakenduse Finance seadistuse käigus teete järgmist.

1. ER-i andmemudeli, ER-i andmemudeli vastenduse ja FatturaPA e-arvete kontekstikonfiguratsioonide importimine.
2. Serdi konfigureerimine, mis on vajalik Itaalia e-arvete digitaalseks allkirjastamiseks.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>ER-i andmemudeli, andmemudeli vastenduse ja vormingute importimine

1. Veenduge, et tööruumis **Elektrooniline aruandlus** oleks konfiguratsioonipakkuja **Äridokumendi teenus** väärtuseks määratud **Aktiivne**.
2. Valige **Hoidlad**.
3. Valige **Globaalne ressurss \> Ava**.
4. Importige **Arvemudel**, **Arvemudeli vastendus** ja **Kliendiarve kontekstimudel**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Itaalia elektrooniliste arvete eksportimise funktsiooni sisselülitamine

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Märkige vahekaardil **Funktsioonid** märkeruut **Lubatud** funktsiooniviite **IT00036** rea puhul.

![FatturaPA funktsiooni sisselülitamine.](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Elektrooniliste dokumentide konfigureerimine

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Valige vahekaardil **Elektrooniline dokument** suvand **Lisa** ja sisestage tabelid, mis on vajalikud Itaalia e-arvete loomiseks.

    - **Tabeli nimi:** kliendiarve tööleht
    - **Tabeli nimi:** projektiarve

3. Määratlege iga tabeli puhul seotud dokumendi kontekst.

    - Valige suvandi **Kliendiarve tööleht** puhul **Kliendiarve kontekst**.
    - Valige suvandi **Projektiarve** puhul **Projektiarve kontekst**.

![Vastusetüüpide seadistamine.](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Elektroonilise arve töötlemine

Rakenduses Finance teete töötlemise käigus järgmist.

1. Itaalia e-arvete loomine elektroonilise arvelduse lisandmooduli kaudu
2. Käivituslogide vaatamine ja töötlemise tulemuste ülevaatamine

### <a name="generate-electronic-invoices"></a>Elektrooniliste arvete loomine

Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist ja funktsiooni **IT00036** aktiveerimist ei saa enam Itaalia e-arvete loomiseks kasutada rakenduse Finance vana protsessi. See asendatakse uue protsessiga **Edasta elektroonilised dokumendid**.

Dokumente saate edastada käsitsi sõltuvalt nõudlusest e-arve dokumentide järele.

> [!NOTE]
> Enne jätkamist veenduge, et Itaalia e-arvete jaoks vajalik seadistus oleks lõpetatud. Lisateavet leiate teemast [Kliendi elektroonilised arved](./emea-ita-e-invoices.md). Pange tähele, et mõni selles teemas kirjeldatud seadistusetapp ei pruugi olla elektroonilise arvelduse lisandmooduli aktiveerimise tõttu saadaval.

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Edasta elektroonilised dokumendid**.
2. Mis tahes dokumendi esimese edastamise korral seadke suvandi **Dokumentide taasedastamine** väärtuseks **Ei**. Kui peate dokumendi teenuse kaudu uuesti edastama, seadke selle suvandi väärtuseks **Jah**.
3. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**, et avada dialoogiboks **Päring**, kus saate luua päringu edastatavate dokumentide valimiseks.

![Elektrooniliste dokumentide edastamise dialoogiboks.](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Filtri päring

1. Konfigureerige dialoogiboksis **Päring** filtreerimistingimused nii müügi- kui ka projektiarvete jaoks või jätke tingimused tühjaks, et kaasata kõik edastamata arved.

    ![Edastamise filtreerimiskriteeriumide seadistamine.](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Valige dialoogiboksi **Päring** sulgemiseks **OK**.
3. Valige **OK**, et edastada valitud dokumendid.

> ![MÄRKUS] Esimesel dokumendi edastamise katsel teenuse kaudu palutakse teil kinnitada ühendus elektroonilise arvelduse lisandmooduliga. Valige **Elektroonilise dokumendi edastusteenusega ühendumiseks klõpsake siin**.

#### <a name="view-submission-logs"></a>Edastuslogide kuvamine

Saate vaadata kõigi edastatud dokumentide edastuslogisid.

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.
2. Valige väljal **Dokumenditüüp** suvand **Kliendiarve tööleht** või **Projektiarve**, et kuvada vajalikud elektroonilised dokumendid.

    ![Dokumendi tüübi valimine edastuslogide kuvamiseks.](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    Veerus **Edastuse olek** toodud väärtus tähistab edastusprotsessi olekut. See näitab, kas protsess käitati nagu konfigureeritud ja kas vajalik on täiendav tegevus.

3. Valige toimingupaanil **Päringud \> Edastuse üksikasjad**, et vaadata edastuse käivituslogide üksikasju.

    ![Edastuslogi üksikasjade vaatamine.](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. Kiirkaardil **Töötlemistegevused** saate vaadata RCS-is seadistatud funktsiooni versioonis konfigureeritud tegevuste käivituslogi. Veerus **Olek** on näha, kas tegevuse käivitamine õnnestus.
5. Kiirkaardil **Tegevusfailid** saate vaadata vahefaile, mis loodi tegevuste käivitamise ajal. Saate valida **Kuva**, et laadida alla XML-väljundfail vormingus **FatturaPA** ja vaadata selle sisu.

## <a name="related-topics"></a>Seotud dokumendid

- [Elektroonilise arvelduse ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arveldusega alustamine](e-invoicing-get-started.md)
- [Seadista elektrooniline häälestus](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]