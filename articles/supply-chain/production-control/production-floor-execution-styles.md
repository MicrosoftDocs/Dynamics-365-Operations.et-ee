---
title: Tootmisosakonna täideviimisliidese laadide määramine
description: Teema selgitab, kuidas konfigureerida vormi juhtelemente nii, et neile rakendataks tootmiskorruse vaikekäitusstiile.
author: johanhoffmann
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 32e49458f6ea7c484bc4200e414d930381b31891
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651970"
---
# <a name="style-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese laadide määramine

[!include [banner](../includes/banner.md)]

Teema selgitab, kuidas konfigureerida vormi juhtelemente nii, et neile rakendataks tootmiskorruse vaikekäitusstiile.

## <a name="forms-and-dialogs"></a>Vormid ja dialoogid

Stiile saab vormile või dialoogile rakendada ainult siis, kui on täidetud järgmised nõuded.

- Kui vorm peaks sarnanema olemasoleva aruande edenemise vormiga, peab teie vormi või dialoogi nimi algama **JmgProductionFloorExecutionCustomInputDialog**.
- Vorm või dialoog võib sisaldada üksikasjade vormiosa. Sellele stiilide rakendamiseks peab detailvormiosa nimi algama väärtusega **JmgProductionFloorExecutionCustomDetailsDialog**.
- Kui vormil või dialoogil peaks olema lihtne vaade, peab lihtvaate nimi algama väärtusega **JmgProductionFloorExecutionCustomDialog**. Lihtsa vaatega vormide näited hõlmavad algusvormi ja kaudse tegevuse vormi.
- Kõik dialoogis olevad juhtelemendid peavad olema konfigureeritud nii, nagu selles teemas kirjeldatud.

> [!IMPORTANT]
> Selle loendi kahes esimeses punktis mainitud funktsioonid nõuavad Supply Chain Managementi versiooni 10.0.19 või uuemat.

Stiile saab **OK** nupule või dialoogile rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nimi algab tähega **OkButtonGroup**.

Stiile saab **Tühista** nupule või dialoogikastile rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nimi algab tähega **CancelButtonGroup**.

## <a name="grid"></a>Tabel

Stiile rakendatakse automaatselt. Spetsiifiline konfiguratsioon ei ole nõutud.

## <a name="card-view"></a>Kaardi vaade

Stiile saab kaardivaate juhtelementidele rakendada ainult siis, kui on täidetud järgmised nõuded.

- Iga kaardivaade sisaldub vormirühmas.
- Grupi nimi algab liitega **CardGroup** (näiteks **CardGroupJobsView**).

Järgmisel joonisel on kujutatud kaardivaade, mille sees pole juhtnuppe.

![Elementideta kaardivaade.](media/pfe-styles-empty-card.png)

Järgmistel joonistel on kujutatud kaardivaateid, mille sees on juhtnupud.

![Kaart elementidega, mis näitavad Hz.](media/pfe-styles-elements.png)

![Kaart elementidega hooldustaotluse jaoks.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Visiitkaart

Stiile saab visiitkaardi juhtelementidele rakendada ainult siis, kui on täidetud järgmised nõuded.

- Iga visiitkaart sisaldub vormirühmas.
- Grupi nimi algab liitega **BusinessCardGroup** (näiteks **BusinessCardGroupJobsList**).

Määrake visiitkaardil järgmised omadused:

- **Laad**: **loend**
- **Laiendatud laad**: **cardList**
- **Mitme valikuga**: **ei**
- **Kuva tulba sildid**: **ei**

![Visiitkaart.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Raadionupp

Stiile saab raadionuppudele rakendada ainult siis, kui on täidetud järgmised nõuded.

- Iga raadionupp sisaldub vormirühmas.
- Grupi nimi algab sõnadega **RadioTextBelow** või **RadioTextRight** olenevalt sellest, kus soovite teksti kuvada.

Määrake raadionupul järgmised omadused:

- **Tumblernupp**: **aktiivne**
- **Tumblernupu väärtus**: **Sees**, kui raadionupp on valitud; muidu **Väljas**

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

- **Nupu kuva**: **TextWithImageLeft**.
- **Normaalne pilt**: see atribuut ei tohi jääda tühjaks. Näiteks kasutage **CoffeeScript**.
- **Tekst**: see atribuut ei tohi jääda tühjaks. Näiteks kasutage **Start Break**.
- **Laius**: **automaatne**.
- **Kõrgus**: **automaatne**.

### <a name="primary-button"></a>Põhinupp

Stiile saab esmasele nupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nimi algab liitega **DefaultButtonGroup** või **PrimaryButtonGroup** (näiteks **DefaultButtonGroup10**).

![Peamine nupp.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Lisanupp

Stiile saab lisanupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Rühma nimi on **Parem paneel** või grupi nimi algab sõnadega **SecondaryButtonGroup**.

![Lisanupp.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Kolmas grupp nuppe

Stiile saab kolmanda grupi nupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Rühma nimi on **Vasak paneel** või grupi nimi algab sõnadega **ThirdButtonGroup**.

![Kolmanda grupi nupp.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Neljanda grupi nupp

Stiile saab neljanda grupi nupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nimi algab tähega **FourthButtonGroup**.

Määrake nupule järgmised omadused:

- **Nupu kuva**: **TextOnly**.
- **Normaalne pilt**: see atribuut ei tohi jääda tühjaks.
- **Tekst**: see atribuut ei tohi jääda tühjaks. Näiteks kasutaeg **Kuva** või **Redigeeri**.
- **Laius**: **automaatne**.
- **Kõrgus**: **automaatne**.

![Neljanda grupi nupp.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Lame nupp

Stiile saab lamedale nupule rakendada ainult siis, kui on täidetud järgmised nõuded.

- Nupp sisaldub vormirühmas.
- Grupi nimi algab tähega **FlatButtonGroup**.

Määrake nupule järgmised omadused:

- **Nupu kuva**: **ImageOnly**.
- **Normaalne pilt**: see atribuut ei tohi jääda tühjaks. Näiteks kasutage **CoffeeScript**.
- **Tekst**: see atribuut ei tohi jääda tühjaks.
- **Laius**: **automaatne**.
- **Kõrgus**: **automaatne**.

![Lame nupp.](media/pfe-styles-flat-button.png)

## <a name="combo-box"></a>Liitboks

Liitkast on kombinatsioon kolmest juhtelemendist: sisendi juhtelement, nupp, mis kustutab sisendi juhtelemendi, ja nupp, mis käivitab otsingu.

Stiile saab liitkastile rakendada ainult siis, kui on täidetud järgmised nõuded.

- Liitkast sisaldub vormirühmas.
- Grupi nimi algab tähega **Combobox**.
- Grupi sees on esimene juhtelement **AxFormStringControl**. See juhtnupp näitab praegust väärtust ja sinna sisestab kasutaja vajaliku väärtuse.
- Teine juhtnupp on **CommonButton** ja selle nimi algab **ClearButton**-ga. See nupp peab sisaldama koodi, mis kasutab nupu kuvamiseks või peitmiseks atribuuti **luba**. Näiteks nupu **Tühjenda** kuvamiseks või peitmiseks, kui kasutaja sisestab sisendjuhtseadmesse teavet, saate kasutada järgmist koodi.

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

    Kasutage nuppu **Tühjenda** meetodi **klõpsatud** jaoks järgmist koodi.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Määrake sisendjuhtelemendi **AxFormStringControl** väärtus, kui vorm lähtestatakse meetodi **init** abil. Kui väärtus ei ole tühi, lubage nupp **Tühjenda**. Kui väärtus on tühi, keelake nupp **Tühjenda**.

- Kolmas juhtnupp on **CommonButton** ja selle nimi algab **SearchButton**-ga.

Järgmisel joonisel on kujutatud kaks liitkasti juhtnuppu. Vasakpoolses liitkastis on tühi tekstikast ja nupp **Tühjenda** on keelatud. Parempoolses liitkastis on tekst ja nupp **Tühjenda** on lubatud.

![Kombineeritud kastid koos nupuga Tühjenda ja ilma.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Kiirfilter

Kiirfiltri juhtelement lisab lehele otsinguvälja. Saate kiirfiltrile stiile rakendada, kui on täidetud järgmised nõuded.

- Kiirfilter sisaldub vormirühmas.
- Grupi nimi algab tähega **SearchInputGroup**.
- Grupi sees on esimene juhtelement **QuickFilter**. (Siin sisestab kasutaja otsingustringi.)
- Teine juhtelement on **FormStaticTextControl** nimega **NumberOfResults**. (See on valikuline ja näitab leitud üksuste arvu, kui see on kaasas.)
- Kolmas juhtnupp on **CommonButton** ja selle nimi algab **ClearButton**-ga.

Järgmisel joonisel on kujutatud kaks kiirfiltri juhtnuppu. Vasakpoolsel kiirfiltril on tühi kiirfilter ja tulemuste arv pole nähtav. Parempoolne kiirfilter sisaldab otsingustringi ja näitab tulemuste arvu.

![Näited kiirfiltri juhtelemendist otsingustringiga ja ilma.](media/pfe-styles-quick-filter.png "Näited kiirfiltri juhtelemendist otsingustringiga ja ilma selleta")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
