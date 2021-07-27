---
title: Microsoft Office stiili kasutajaliides äridokumendi halduses
description: See teema selgitab kuidas kasutada uut kasutajaliidest elektroonilise aruandluse (ER) raamistikku äridokumendi halduse funktsioonis.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e8a3782e5beb7d16accc0a56447d5db1f1376dd8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350180"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office stiili kasutajaliides äridokumendi halduses

[!include [banner](../includes/banner.md)]

Äridokumendi haldus võimaldab ärikasutajatel redigeerida äridokumendi malle Microsoft 365 teenuse või asjakohase Microsoft Office'i töölauarakendusega. Muudatused võivad hõlmata kujunduse muudatusi või uusi juurutusi, või kasutajad võivad lisada kohatäited, et kaasata täiendavaid andmeid, ilma et peaksite lähtekoodi muutma. Lisateavet äridokumentide haldusega töötamise kohta vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).

Uus kasutajaliides (UI) on selgem ja seda on mugavam kasutada. **Äridokumendi** ala näitab ainult malle, mis on saadaval praegusele pakkujale. Eelmises kasutajaliideses loetleti vahekaardil **Mall** kõik mallid, mis olid saadaval kõigile pakkujatele. Näitab kõiki malle, mille on loonud ja redigeerinud iga sama rolliga kasutaja.

Saate kasutada **Uue dokumendi** nuppu, mis võimaldab luua ja redigeerida malli elektroonilise aruandluse (ER) vormingu konfiguratsioonis, mida pakub teine pakkuja. Selle teema näites on pakkuja Microsoft. Teise võimalusena saate malli luua oma malli Exceli vormingus üles laadides.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

[Äridokumendi halduse abil uue äridokumendi loomise](https://youtu.be/gAIYl-mM_pw) video (näidatud ülal) leiab [esitlusloendist Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) rakenduses YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Tee uus dokumendi kasutajaliides äridokumentide halduses kättesaadavaks

Et alustada uue dokumendi kasutajaliidese kasutamist äridokumentide halduses peate **Office'i sarnase kasutajaliidese kogemuse äridokumendi halduses** **Funktsiooni halduse** tööruumis sisse lülitama.

Kõigi juriidiliste isikute jaoks selle funktsiooni sisselülitamiseks toimige järgmiselt.

1. Valige **Fuktsioonide halduse** tööruumis vahekaardil **Kõik** loendis funktsioon **Office'i sarnase kasutajaliidese kogemus äridokumendi haldamises**.
2. Valitud funktsiooni lubamiseks valige **Luba kohe**.
3. Uue funktsiooni kasutamiseks värskenda lehte.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Muutke teiste pakkujate malle

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.

    ![Äridokumentide halduse tööruum.](./media/BDM_overview_new_template1.png)

2. Vahekaardil **Vali** valige mallina kasutatav dokument ja seejärel valige **Loo dokument**.

    ![Äridokumentide dialoogiboks.](./media/BDM_overview_new_template2.png)

3. Muutke vajadusel pealkiri uue dialoogiboksi väljal **Pealkiri**. Pealkirja tekstiga nimetatakse ise tekkivat uut ER-vormingu seadistust. Seda muudetavat malli sisaldava seadistuse (**Kliendi FTI aruande (GER) koopia**) mustandit ja ER-vormingu praeguse kasutaja puhul. ER-vormingu põhiseadistuse muutmata algset malli kasutatakse selle ER-vormingu käivitamiseks kõikide kasutajate puhul.
4. Muutke väljal **Nimi** isetekkiva muudetava malli esimese redaktsiooni nime.
5. Väljal **Kommentaar** värskendage isetekkiva muudetava malli redaktsiooni märkusi.
6. Muutmis alustamise kinnitamiseks valige **OK**.

    ![Dokumendi loomise dialoogiboks.](./media/BDM_overview_new_template3.png)

**Uue dokumendi** nuppu kasutatakse malli loomiseks ja redigeerimiseks elektroonilise aruandluse (ER) vormingu konfiguratsioonis, mida pakub teine pakkuja. Selles näites on pakkuja Microsoft. Kui valite suvandi **Uus dokument**, saate vaadata kõiki praeguse ja teiste pakkujate omanduses olevaid malle. Pärast malli valimist avatakse see redigeerimiseks. Muudetud malli saab seejärel muuta uues ise loodavas ER-vormingus seadistusega.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Olemasolevat Exceli vormingut kasutava malli üleslaadimine
Enne malli üleslaadimist vajaliku teabe esitamiseks toimige järgmiselt.

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.

    ![Äridokumentide halduse tööruum.](./media/BDM_overview_new_template1.png)
    
2. Klõpsake lehe **Uue malli loomine** vahekaardi **Üleslaadimine** vahekaardil **Mall** nuppu **Sirvi**, et leida ja valida Exceli fail, mida soovite mallina kasutada. Jaotises **Mall** täidetakse väljad **Pealkiri** ja **Kirjeldus** automaatselt. Nad määravad automaatselt loodava uue ER-vormingu konfiguratsiooni nime ja kirjelduse. Vajadusel saate neid välju redigeerida.
3. Määrake jaotise **Dokumendi liik** väljal **Nimi** äridokumendi liik. Seda väärtust kasutatakse õige andmeallika (st ER-mudeli konfiguratsiooni) otsimiseks.

    ![Malli vahekaart.](./media/BDM_overview_new_UI_import_21.jpg)

4. Klõpsake menüü **Andmeallikas** kiirkaardil **Filter** nuppu **Rakenda filter**. Jaotises **Andmeallikas** täidetakse väli **Nimi** automaatselt või saate väärtuse käsitsi valida. Filtri abil saate otsida sobivat andmeallika nime nime, kirjelduse, riigi/regiooni tähise ja äridokumendi liigi alusel.

    ![Andmeallika vahekaart.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > Kiirkaarti **Filter** kasutatakse õige andmeallika (st ER-mudeli konfiguratsiooni) otsimiseks. Üleslaaditava dokumendi jaoks sobivaima andmeallika leidmiseks saate redigeerida kõiki filtrivälju.
    > 
    > Kiirkaardi **Filter** tingimusi kasutatakse **OR**-tingimustena.
    
5. Valige vahekaardil **Vastendamine** käsk **Tuvasta automaatselt**. Väli **Ruudi definitsioon** täidetakse automaatselt või saate väärtuse käsitsi valida. Sellel vahekaardil kuvatakse malli ja mudeli elementide lõppvastendus.

    ![Vastendamine vahekaart.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Jaotise **Malli struktuur** vastendamine kasutab andmeallika siltide või kirjelduste täielikku vastendust kasutaja keeles ja malli lahtrinimes.

6. Malli loomise kinnitamiseks ja redigeerimisprotsessi alustamiseks valige **Loo dokument**.

Lisateavet vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).

Kui elektroonilises aruandluses pole teenusepakkujat, saate selle luua. Kui aktiivset pakkujat pole, saate selle aktiveerida.

- Pakkuja loomiseks muutke väljal **Nimi** teenusepakkuja nime, värskendage uue pakkuja välja **Interneti-aadress** ja klõpsake kinnitamiseks nuppu **OK**.

    ![BDM-is uue pakkuja loomine.](./media/bdm_create_provider.png)
    
- Olemasoleva pakkuja aktiveerimiseks valige väljal **Konfiguratsioonipakkuja** pakkuja pakkuja nimi ja valige **OK**, et seada pakkuja aktiivseks.

    ![Pakkuja aktiveerimine BDM-is.](./media/bdm_choose_provider.png)

> [!NOTE]
> Iga BDM-i mall viitab pakkujale kui konfiguratsiooni autorile. Seetõttu on malli jaoks vaja aktiivset pakkujat.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
