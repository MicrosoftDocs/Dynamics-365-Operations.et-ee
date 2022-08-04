---
title: Microsoft Office äridokumendihalduse (sisaldab videot) laadne kasutajaliides
description: See artikkel selgitab, kuidas kasutada uut kasutajaliidest elektroonilise aruandluse (ER) raamistiku äridokumendihalduse funktsioonis.
author: v-anamir
ms.date: 01/05/2022
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
ms.openlocfilehash: 208cfc91f11d4893785538ce4874e85a5725e993
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109256"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office stiili kasutajaliides äridokumendi halduses

[!include [banner](../includes/banner.md)]

Äridokumendi haldus võimaldab ärikasutajatel redigeerida äridokumendi malle teenuse Microsoft Office 365 või vastava Microsoft Office töölauarakendusega. Muudatused võivad hõlmata kujunduse muudatusi või uusi juurutusi, või kasutajad võivad lisada kohatäited, et kaasata täiendavaid andmeid, ilma et peaksite lähtekoodi muutma. Lisateavet äridokumentide haldusega töötamise kohta vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).

Uus kasutajaliides (UI) on selgem ja seda on mugavam kasutada. Äridokumendi **alas** kuvatakse [...](tasks/er-configuration-provider-mark-it-active-2016-11.md)[ainult](general-electronic-reporting.md#Provider) mallid, mis on praeguse aktiivse pakkuja omad ja mis asuvad dynamics 365 Finance praeguses eksemplaris. Eelmises KASUTAJALIIDESEs loetles **malli vahekaart** kõik mallid, mis olid mis tahes pakkuja jaoks saadaval. Näitab kõiki malle, mille on loonud ja redigeerinud iga sama rolliga kasutaja.

Saate **kasutada** **·**[nuppu Uus dokument Äridokumendi halduse tööruumis malli loomiseks ja redigeerimiseks elektroonilise aruandluse (ER)](general-electronic-reporting.md)[vormingus](general-electronic-reporting.md#Configuration) konfiguratsioonis, mille on andnud teine pakkuja ja mis asub praeguses Finantside eksemplaris, või laadida uus mall Exceli töövihikust üles. Lisaks sellele saate versioonis 10.0.25 ja uuemas versioonis kasutada nuppu Uus dokument malli loomiseks ja redigeerimiseks ER-vormingu konfiguratsioonis, **mis** on talletatud globaalses hoidlas [.](general-electronic-reporting.md#Repository)

Selle artikli näidetes on aktiivne pakkuja Contoso ja te kasutate seda Microsofti antud mallil põhineva malli loomiseks. Teise võimalusena saate malli luua oma malli Exceli vormingus üles laadides.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Äridokumendi [haldus video abil uue äridokumendi loomine](https://youtu.be/gAIYl-mM_pw) (vt ülal kuvatud) [sisaldub finantsis ja toimingutes, mille](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) kohta on saadaval YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Tee uus dokumendi kasutajaliides äridokumentide halduses kättesaadavaks

Et alustada uue dokumendi kasutajaliidese kasutamist äridokumentide halduses peate **Office'i sarnase kasutajaliidese kogemuse äridokumendi halduses** **Funktsiooni halduse** tööruumis sisse lülitama.

Kõigi juriidiliste isikute jaoks selle funktsiooni sisselülitamiseks toimige järgmiselt.

1. Valige **Fuktsioonide halduse** tööruumis vahekaardil **Kõik** loendis funktsioon **Office'i sarnase kasutajaliidese kogemus äridokumendi haldamises**.
2. Valitud funktsiooni lubamiseks valige **Luba kohe**.
3. Uue funktsiooni kasutamiseks värskenda lehte.

## <a name="add-or-activate-a-provider"></a>Pakkuja lisamine või aktiveerimine

Äridokumendi iga mall talletatakse ER-vormingu konfiguratsioonis, mis on märgitud kindla konfiguratsioonipakkuja omaks. Uue malli loomisel luuakse selle ootele võtte jaoks uus ER-vormingu konfiguratsioon. Seetõttu peab pakkuja olema selle konfiguratsiooni jaoks identifitseeritud. ER-raamistiku aktiivset pakkujat kasutatakse sel eesmärgil. Kui ER-is puudub pakkuja, saate selle luua. Kui aktiivset pakkujat *pole*, saate aktiveerida ühe olemasolevatest pakkujatest. Kui see on vajalik, siis avatakse dialoogiboks pakkuja lisamiseks või aktiveerimiseks, samal ajal kui alustate uue malli lisamist.

### <a name="add-a-new-provider"></a>Uue pakkuja lisamine

Uue pakkuja loomiseks järgige konfiguratsioonipakkuja dialoogis **neid samme**.

1.  **Sisestage uue pakkuja** nimi **vahekaardi Vali** konfiguratsioonipakkuja väljale Nimi.
2.  Sisestage **väljale Interneti-aadress** uue pakkuja Interneti-aadress (URL). 
3.  Valige nupp **OK**.

    ![Uue pakkuja loomine äridokumendihalduses](./media/bdm_create_provider.png)

Lisatud pakkuja aktiveeritakse automaatselt.

### <a name="activate-a-provider"></a>Pakkuja aktiveerimine

Pakkuja aktiveerimiseks järgige konfiguratsioonipakkuja dialoogis **neid samme**.

1.  **Valige vahekaardi Vali** konfiguratsioonipakkuja väljal **Konfiguratsioonipakkuja** pakkuja.
2.  Valige nupp **OK**.

    ![Pakkuja aktiveerimine Äridokumendihalduses](./media/bdm_choose_provider.png)

Valitud pakkuja aktiveeritakse.

> [!NOTE]
> Iga äridokumendi halduse mall asub ER-vormingu konfiguratsioonis, mis viitab pakkujale kui konfiguratsiooni autorile. Seetõttu on iga malli jaoks vaja aktiivset pakkujat.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Redigeerige malli, mis kuulub teisele pakkujale.

See näide näitab **, kuidas kasutada nuppu Uus dokument** **Äridokumendihalduse** tööruumis malli loomiseks ja redigeerimiseks ER-vormingu konfiguratsioonis, mille on andnud teine pakkuja ja mis asub praeguses finantseksemplaris. Selles näites on aktiivne pakkuja Contoso, mis kasutab Microsofti antud ER-vormingu konfiguratsiooni. Pärast uue **dokumendi valimist** kuvab uue mallilehe loomise vahekaart Vali kõik praeguse finantseksemplari mallid, **mis** kuulub **praegusele** pakkujale ja teistele pakkujatele. Valige selle avamiseks mall. Seejärel saate luua mallist uue redigeeritava koopia. Redigeeritud mall talletatakse automaatselt loodud uude ER-vormingu konfiguratsiooni.

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.

    ![Äridokumentide halduse tööruum.](./media/BDM_overview_new_template1.png)

2. **Valige vahekaardil Vali uue** mallilehe loomine **mallina** kasutamiseks dokument ja seejärel valige suvand Loo **dokument**.

    ![Äridokumentide dialoogiboks.](./media/BDM_overview_new_template2.png)

3. Muutke vajadusel pealkiri uue dialoogiboksi väljal **Pealkiri**. Pealkirja tekstiga nimetatakse ise tekkivat uut ER-vormingu seadistust. Seda muudetavat malli sisaldava seadistuse (**Kliendi FTI aruande (GER) koopia**) mustandit ja ER-vormingu praeguse kasutaja puhul. ER-vormingu põhiseadistuse muutmata algset malli kasutatakse selle ER-vormingu käivitamiseks kõikide kasutajate puhul.
4. Muutke väljal **Nimi** isetekkiva muudetava malli esimese redaktsiooni nime.
5. Väljal **Kommentaar** värskendage isetekkiva muudetava malli redaktsiooni märkusi.
6. Muutmis alustamise kinnitamiseks valige **OK**.

    ![Dokumendi loomise dialoogiboks.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Laadige üles mall, mis kasutab olemasolevat Exceli töövihikut.

See näide näitab, kuidas **kasutada nuppu Uus dokument** **Äridokumendihalduse** tööruumis malli loomiseks ja redigeerimiseks ER-vormingu konfiguratsioonis, mis põhineb saadaoleval Exceli töövihikul. Selles näites on aktiivne pakkuja Contoso ning te kasutate Microsofti antud ER-i [andmemudelit](er-overview-components.md#data-model-component) ja ER-mudeli [vastendamise](er-overview-components.md#model-mapping-component) konfiguratsioone. Pärast uue **dokumendi valimist** valige **uue mallilehe** loomise **vahekaardil Üleslaadimine**. Seal saate määrata Exceli töövihiku üleslaadimise üksikasjad. Pärast Exceli töövihiku üleslaadimist muutub see äridokumendi malliks, mis on redigeerimiseks avatud. Redigeeritud mall talletatakse automaatselt loodud uude ER-vormingu konfiguratsiooni.

Enne malli üleslaadimist vajaliku teabe esitamiseks toimige järgmiselt.

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.
2. Klõpsake lehe **Uue malli loomine** vahekaardi **Üleslaadimine** vahekaardil **Mall** nuppu **Sirvi**, et leida ja valida Exceli fail, mida soovite mallina kasutada. Jaotises **Mall** täidetakse väljad **Pealkiri** ja **Kirjeldus** automaatselt. Nad määravad automaatselt loodava uue ER-vormingu konfiguratsiooni nime ja kirjelduse. Vajadusel saate neid välju redigeerida.
3. Määrake jaotise **Dokumendi liik** väljal **Nimi** äridokumendi liik. Seda väärtust kasutatakse õige andmeallika (st ER-mudeli konfiguratsiooni) otsimiseks.

    ![Uue mallilehe loomise vahekaardi Üleslaadimine vahekaart Mall.](./media/BDM_overview_new_UI_import_21.jpg)

4. Klõpsake menüü **Andmeallikas** kiirkaardil **Filter** nuppu **Rakenda filter**. Jaotises **Andmeallikas** täidetakse väli **Nimi** automaatselt või saate väärtuse käsitsi valida. Filtri abil saate otsida sobivat andmeallika nime nime, kirjelduse, riigi/regiooni tähise ja äridokumendi liigi alusel.

    ![Uue mallilehe loomise vahekaardi Üleslaadimine andmeallikas.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Kiirkaarti **Filter** kasutatakse õige andmeallika (st ER-mudeli konfiguratsiooni) otsimiseks. Üleslaaditava dokumendi jaoks sobivaima andmeallika leidmiseks saate redigeerida kõiki filtrivälju.
    > 
    > Kiirkaardi **Filter** tingimusi kasutatakse **OR**-tingimustena.

5. Valige vahekaardil **Vastendamine** käsk **Tuvasta automaatselt**. Väli **Ruudi definitsioon** täidetakse automaatselt või saate väärtuse käsitsi valida. Sellel vahekaardil kuvatakse malli ja mudeli elementide lõppvastendus.

    ![Uue mallilehe loomise vahekaardi Üleslaadimine vastendus.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Jaotise **Malli struktuur** vastendamine kasutab andmeallika siltide või kirjelduste täielikku vastendust kasutaja keeles ja malli lahtrinimes.

6. Malli loomise kinnitamiseks ja redigeerimisprotsessi alustamiseks valige **Loo dokument**.

Lisateavet vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Laadige mall globaalsest hoidlast üles

See näide **näitab** **·**, kuidas kasutada nuppu Uus dokument Äridokumendihalduse tööruumis malli loomiseks ja redigeerimiseks Microsofti antud ER-vormingu konfiguratsioonis, mis asub globaalses hoidlas. Selles näites on aktiivne pakkuja Contoso, mis kasutab Microsofti antud ER-vormingu konfiguratsiooni. Pärast uue dokumendi **valimist** näitab vahekaardi Impordi globaalsest hoidlast vahekaardil Uue malli loomine kõiki äridokumendi malle, mida talletatakse globaalses hoidlas, **kuid** mis on **praeguses** finantseksemplaris puudu. Pärast malli valimist imporditakse see globaalsest hoidlast praegusesse finantseksemplari, et luua uus redigeeritav koopia. Redigeeritud mall talletatakse automaatselt loodud uude ER-vormingu konfiguratsiooni.

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.
2. Valige mallina **kasutamiseks** **dokument** uue mallilehe vahekaardilt Impordi globaalsest hoidlast ja seejärel valige suvand **Loo dokument.**

    ![Impordib globaalsest hoidlast vahekaardilt Uue malli lehe loomine.](./media/BDM_overview_new_template22.png)

3. Valige teateaknas **Jah**, et kinnitada, et soovite valitud dokumendi globaalsest hoidlast importida praegusesse finantseksemplari. Kui teilt küsitakse autoriseerimist, järgige ekraanil olevaid juhiseid.
4. Muutke vajadusel pealkiri uue dialoogiboksi väljal **Pealkiri**. Pealkirja tekstiga nimetatakse ise tekkivat uut ER-vormingu seadistust. Selle konfiguratsiooni mustandversioon (Märgukirjamärkuse **(Excel) koopia**) sisaldab redigeeritud malli ja seda kasutatakse praeguse kasutaja ER-vormingu käivitamiseks. ER-vormingu põhiseadistuse muutmata algset malli kasutatakse selle ER-vormingu käivitamiseks kõikide kasutajate puhul.
5. Muutke väljal **Nimi** isetekkiva muudetava malli esimese redaktsiooni nime.
6. Väljal **Kommentaar** värskendage isetekkiva muudetava malli redaktsiooni märkusi.
7. Muutmis alustamise kinnitamiseks valige **OK**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

