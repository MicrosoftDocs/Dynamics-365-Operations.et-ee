---
title: Tootmisosakonna täideviimisliidese laadide määramine
description: Teema selgitab, kuidas konfigureerida vormi juhtelemente nii, et neile rakendataks tootmiskorruse vaikekäitusstiile.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ef39dc6414f0afdadd4a4b5a41e1fb1fe60e4974
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790886"
---
# <a name="style-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese laadide määramine

[!include [banner](../includes/banner.md)]

Teema selgitab, kuidas konfigureerida vormi juhtelemente nii, et neile rakendataks tootmiskorruse vaikekäitusstiile.

## <a name="forms-and-dialogs"></a>Vormid ja dialoogid

Stiile saab vormile või dialoogile rakendada ainult siis, kui on täidetud järgmised nõuded.

- Kui vorm peaks sarnanema olemasoleva aruande edenemisvormiga, peavad teie vormi või dialoogi nimi alg olema `JmgProductionFloorExecutionCustomInputDialog`.
- Vorm või dialoog võib sisaldada üksikasjade vormiosa. Stiilide rakendamiseks peab üksikasjavormi osa nimi alg olema `JmgProductionFloorExecutionCustomDetailsDialog`.
- Kui vormil või dialoogil peaks olema lihtne vaade, peab lihtvaate nimi alg olema `JmgProductionFloorExecutionCustomDialog`. Lihtsa vaatega vormide näited hõlmavad algusvormi ja kaudse tegevuse vormi.
- Kõik dialoogi juhtelemendid tuleb konfigureerida selles teemas kirjeldatud viisil.

> [!IMPORTANT]
> Selle loendi kahes esimeses punktis mainitud funktsioonid nõuavad Supply Chain Managementi versiooni 10.0.19 või uuemat.

Stiile saab **OK** nupule või dialoogile rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nime algus on `OkButtonGroup`.

Stiile saab **Tühista** nupule või dialoogikastile rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nime algus on `CancelButtonGroup`.

### <a name="header"></a>Päis

Järgmine illustratsioon näitab tüüpilist vormi või dialoogi päist.

![Tüüpiline vormi või dialoogi päis.](media/pfe-styles-header.png "Vormi või dialoogi tüüpiline päis")

Päised luuakse sellise struktuuri abil, nagu näidatud Visual Studio järgmises illustratsioonis.

![Tüüpiline koodistruktuur päise loomiseks.](media/pfe-styles-header-code-structure.png "Tüüpiline koodistruktuur päise loomiseks")

Päisele teksti lisamiseks kasutage järgmist näidet.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Oma päisekoodi kirjutamisel rakendage järgmisi reegleid:

- Põhigrupi nimi peab olema `TableRowHeaderGroup`.
- Iga tekstiblokk (täpiga eraldatud) peab alg `HeaderFieldWithSeparatorText` olema.
- Viimase teksti nimi peab alg olema `HeaderFieldText`.
- `CaptionImage` võib vahele jätta.

### <a name="progress-indicator"></a>Edenemisenäidik

Saate kaasata edenemisnäidiku, mis kuvatakse päisest paremal. Järgmine illustratsioon näitab edenemisnäidikut.

![Tavaline edenemisindikaator.](media/pfe-styles-header-progress.png "Tavaline edenemisindikaator")

Edenemisnäidiku näitamiseks peab tekstivälja nimi olema `ShowProgress`.

## <a name="grid"></a>Tabel

Stiile rakendatakse automaatselt. Spetsiifiline konfiguratsioon ei ole nõutud.

Ruudustikul peaks olema laad ja kohandatud vormi meetod tuleb `TabularView``run()` üle kirjutada, sest uut ruudustikku ei toetata veel. Lisage järgmine kood.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Põhivaate andmete värskendamiseks võite soovida kasutada midagi `this.parmParentForm().updateLayout();` sellist nagu `click` tegevuse puhul. (Näitena vaadake `JmgProductionFloorExecutionReportFeedbackAction` klassi.) Kontrollige ainult, `parmDataSource` et see on `init` seadistatud teie uue vormi `formCaller.parmDataSource(this.dataSource(1));` () meetodis. Näitena vaadake `JmgProductionFloorExecutionMainGrid` vormi.

## <a name="card-view"></a>Kaardi vaade

Stiile saab kaardivaate juhtelementidele rakendada ainult siis, kui on täidetud järgmised nõuded.

- Iga kaardivaade sisaldub vormirühmas.
- Grupi nimi algab `CardGroup` sellega (nt `CardGroupJobsView`).

Järgmisel joonisel on kujutatud kaardivaade, mille sees pole juhtnuppe.

![Elementideta kaardivaade.](media/pfe-styles-empty-card.png)

Järgmistel joonistel on kujutatud kaardivaateid, mille sees on juhtnupud.

![Kaart elementidega, mis näitavad Hz.](media/pfe-styles-elements.png)

![Kaart elementidega hooldustaotluse jaoks.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Visiitkaart

Stiile saab visiitkaardi juhtelementidele rakendada ainult siis, kui on täidetud järgmised nõuded.

- Iga visiitkaart sisaldub vormirühmas.
- Grupi nimi algab `BusinessCardGroup` sellega (nt `BusinessCardGroupJobsList`).

Määrake visiitkaardil järgmised omadused:

- **Stiil:** *loend*
- **Laiendatud laad:** *kaardiloend*
- **Mitme valikuga:** *ei*
- **Kuva veerusildid:** *ei*

![Visiitkaart.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Raadionupp

Stiile saab raadionuppudele rakendada ainult siis, kui on täidetud järgmised nõuded.

- Iga raadionupp sisaldub vormirühmas.
- Grupi nimi algab `RadioTextBelow` tekstiga `RadioTextRight` või sõltuvalt sellest, kus soovite teksti kuvada.

Määrake raadionupul järgmised omadused:

- **Tumblernupp:** *kontrolli*
- **Tumbleri** *väärtus:* sees, kui raadionupp tuleb valida; muul juhul välja *lülitatud*

Järgmisel joonisel on näide, kus tekst kuvatakse raadionuppude all.

![Alloleva tekstiga raadionupud.](media/pfe-styles-radio-text-below.png)

Järgmisel joonisel on näide, kus tekst kuvatakse raadionuppudest paremal.

![Paremal oleva tekstiga raadionupud.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Internet Explorer brauseri raadionupud

Internet Explorer brauseris raadionuppude stiile ei toetata. Järgmisel joonisel on näidatud, kuidas raadionupud rakenduses Internet Explorer välja näevad.

![Internet Explorer brauseri raadionupud.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Nööbid

Stiile saab nuppudele rakendada ainult siis, kui on täidetud järgmised nõuded.

- Iga nuppude grupp sisaldub vormirühmas. Kõik rühma nupud on sama stiiliga.
- Grupi nimele nõudeid ei esitata.

Määrake nuppudele järgmised omadused:

- **Nupu kuva:** *TextWithImageLeft*
- **Tavaline pilt:** see atribuut ei saa olla tühi. Näiteks kasutage *CoffeeScript*.
- **Tekst:** see atribuut ei saa olla tühi. Näiteks kasutage *Start Break*.
- **Laius:** *Automaatne või* *SizeToContent*
- **Kõrgus:** *Automaatne või* *SizeToContent*

### <a name="primary-button"></a>Põhinupp

Stiile saab esmasele nupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nimi algab `DefaultButtonGroup` järgmisega või `PrimaryButtonGroup` (nt `DefaultButtonGroup10`).

![Peamine nupp.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Lisanupp

Stiile saab lisanupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nimi on **Parem** paneel või grupi nimi `SecondaryButtonGroup` algab.

![Lisanupp.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Kolmas grupp nuppe

Stiile saab kolmanda grupi nupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nimi on **Vasak** paneel või grupi nimi `ThirdButtonGroup` algab.

![Kolmanda grupi nupp.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Neljanda grupi nupp

Stiile saab neljanda grupi nupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nime algus on `FourthButtonGroup`.

Määrake nupule järgmised omadused:

- **Nupu kuvamine:** *TextOnly*
- **Tavaline pilt:** see atribuut peab olema tühi.
- **Tekst:** see atribuut ei saa olla tühi. Näiteks kasutaeg *Kuva* või *Redigeeri*.
- **Laius:** *automaatne*
- **Kõrgus:** *automaatne*

![Neljanda grupi nupp.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Lame nupp

Stiile saab lamedale nupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nime algus on `FlatButtonGroup`.

Määrake nupule järgmised omadused:

- **Nupu kuvamine:** *ImageOnly*
- **Tavaline pilt:** see atribuut ei saa olla tühi. Näiteks kasutage *CoffeeScript*.
- **Tekst:** see atribuut peab olema tühi.
- **Laius:** *Automaatne või* *SizeToContent*
- **Kõrgus:** *Automaatne või* *SizeToContent*

![Lame nupp.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Nupp Jätka

Laade saab rakendada nupuga Jätka ainult juhul, kui järgmised nõuded on täidetud:

- Nupp sisaldub vormirühmas.
- Grupi nime algus on `ContinueButtonGroup`.

Määrake nupule järgmised omadused:

- **Nupu kuvamine:** *ImageOnly*
- **Tavaline pilt:** *edasi*
- **Tekst:** see atribuut peab olema tühi.
- **Laius:** *Automaatne või* *SizeToContent*
- **Kõrgus:** *Automaatne või* *SizeToContent*

![Nupp Jätka.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Liitboks

Liitkast on kombinatsioon kolmest juhtelemendist: sisendi juhtelement, nupp, mis kustutab sisendi juhtelemendi, ja nupp, mis käivitab otsingu.

Stiile saab liitkastile rakendada ainult siis, kui on täidetud järgmised nõuded.

- Liitkast sisaldub vormirühmas.
- Grupi nime algus on `Combobox`.
- Grupis on esimene juhtelement `AxFormStringControl` juhtelement. See juhtnupp näitab praegust väärtust ja sinna sisestab kasutaja vajaliku väärtuse.
- Teine juhtelement on juhtelement `CommonButton` ja selle nimi algab. `ClearButton` See nupp peab sisaldama koodi, mis `enable` kasutab atribuuti nupu näitamiseks või peitmiseks. Näiteks nupu **Tühjenda** kuvamiseks või peitmiseks, kui kasutaja sisestab sisendjuhtseadmesse teavet, saate kasutada järgmist koodi.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Teil peaks olema üks meetod, kus andmed määratakse sisendjuhtelemendis. Lubage sellel meetodil nupp **Tühjenda**. Siin on näide.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Kasutage nupu Tühjenda `clicked` meetodi puhul järgmist **·** koodi.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Seadistage sisendkontrolli `AxFormStringControl` väärtus, kui vorm lähtestatakse meetodi `init` abil. Kui väärtus ei ole tühi, lubage nupp **Tühjenda**. Kui väärtus on tühi, keelake nupp **Tühjenda**.

- Kolmas juhtelement on juhtelement `CommonButton` ja selle nimi algab. `SearchButton`

Järgmisel joonisel on kujutatud kaks liitkasti juhtnuppu. Vasakpoolses liitkastis on tühi tekstikast ja nupp **Tühjenda** on keelatud. Parempoolses liitkastis on tekst ja nupp **Tühjenda** on lubatud.

![Kombineeritud kastid koos nupuga Tühjenda ja ilma.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Kiirfilter

Kiirfiltri juhtelement lisab lehele otsinguvälja. Saate kiirfiltrile stiile rakendada, kui on täidetud järgmised nõuded.

- Kiirfilter sisaldub vormirühmas.
- Grupi nime algus on `SearchInputGroup`.
- Grupis on esimene juhtelement `QuickFilter` juhtelement. (See juhtelement on seal, kuhu kasutaja sisestab otsingustringi.)
- Teine juhtelement on `FormStaticTextControl``NumberOfResults` nimi. (See juhtelement on valikuline. Kui see on kaasatud, kuvatakse siin leitud kaupade arv.)
- Kolmas juhtelement on juhtelement `CommonButton` ja selle nimi algab. `ClearButton`

Järgmisel joonisel on kujutatud kaks kiirfiltri juhtnuppu. Vasakpoolsel kiirfiltril on tühi kiirfilter ja tulemuste arv pole nähtav. Parempoolne kiirfilter sisaldab otsingustringi ja näitab tulemuste arvu.

![Näited kiirfiltri juhtelemendist otsingustringiga ja ilma.](media/pfe-styles-quick-filter.png "Näited kiirfiltri juhtelemendist otsingustringiga ja ilma selleta")

## <a name="center-align-elements-on-a-tab"></a>Joonda elemendid vahekaardil keskele

Elementide joondamiseks vahekaardi keskel peab grupi nimi alg olema ja `TabContentGroup` grupil peavad olema järgmised atribuudid:

- **Laiuse režiim:**`SizeToAvailable`
- **Kõrguse režiim:**`SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Ruudustiku, üksikasjaliku osa ja kiirfiltri joondamine

Kohandatud ruudustiku, detailide osa ja kiire filtri korraldamiseks nii, et need sarnaneksid standardse kujundusega, pidage silmas järgmisi punkte, kui panete need kõik kokku:

- Kui ruudustikul on kiirfilter, peaksid nii ruudustik kui ka kiirfilter olema grupi sees, mille nimi `GridGroup` algab.
- Stiilide rakendamiseks üksikasjaosale peab grupi nimi alg olema `DetailInformationGroup` järgmine:

Järgmine näide näitab tüüpilist ruudustikku, mis sisaldab kiirfiltrit ja üksikasjalist osa paremal.

![Tavaline ruudustik, mis sisaldab kiirfiltri ja üksikasjaliku osa.](media/pfe-styles-align-grid.png "Tavaline ruudustik, mis sisaldab kiirfiltri ja üksikasjaliku osa")

Ruudustiku, üksikasjaliku ja kiire filtri loomiseks saate kasutada järgmist struktuuri, mida näidatakse järgmisel Visual Studio joonisel.

![Tüüpiline koodistruktuur, mis joondab ruudustiku, üksikasjaliku osa ja kiirfiltri.](media/pfe-styles-header-code-structure2.png "Tüüpiline koodistruktuur, mis joondab ruudustiku, üksikasjaliku osa ja kiirfiltri")

## <a name="additional-resources"></a>Lisaressursid

- [Tootmisosakonna täideviimisliidese kohandamine](production-floor-execution-customize.md)
- [Tootmisosakonna täideviimisliidese kujundamine](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
