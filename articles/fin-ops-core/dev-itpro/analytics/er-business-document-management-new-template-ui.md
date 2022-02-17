---
title: Microsoft Office-stiilis kasutajaliides äridokumendi halduses (sisaldab videot)
description: See teema selgitab kuidas kasutada uut kasutajaliidest elektroonilise aruandluse (ER) raamistikku äridokumendi halduse funktsioonis.
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
ms.openlocfilehash: e33830e2147d92ad5ee53ad11da55a50613b8ef9
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074737"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office stiili kasutajaliides äridokumendi halduses

[!include [banner](../includes/banner.md)]

Äridokumendi haldus võimaldab ärikasutajatel redigeerida äridokumendi malle teenuse Microsoft Office 365 või vastava Microsoft Office töölauarakendusega. Muudatused võivad hõlmata kujunduse muudatusi või uusi juurutusi, või kasutajad võivad lisada kohatäited, et kaasata täiendavaid andmeid, ilma et peaksite lähtekoodi muutma. Lisateavet äridokumentide haldusega töötamise kohta vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).

Uus kasutajaliides (UI) on selgem ja seda on mugavam kasutada. Äridokumendi **alal** kuvatakse ainult mallid, mis kuuluvad praegusele [aktiivsele](tasks/er-configuration-provider-mark-it-active-2016-11.md)[pakkujale](general-electronic-reporting.md#Provider) ja asuvad praegusel eksemplaril Dynamics 365 Finance. Eelmises kasutajaliideses loetleti vahekaardil **Mall** kõik mallid, mis olid mis tahes pakkuja jaoks saadaval. Näitab kõiki malle, mille on loonud ja redigeerinud iga sama rolliga kasutaja.

Äridokumendihalduse **tööruumis saate kasutada** nuppu **Uus dokument**, et luua ja redigeerida malli elektroonilise aruandluse (ER) [vormingus](general-electronic-reporting.md)[,](general-electronic-reporting.md#Configuration) mille pakub mõni muu pakkuja ja mis asub praeguses finance'i eksemplaris, või laadida üles uus mall Exceli töövihikust. Lisaks saate versioonis 10.0.25 ja uuemas versioonis kasutada **nuppu Uus dokument** malli loomiseks ja redigeerimiseks ER-vormingus konfiguratsioonis, mis on talletatud globaalsesse [hoidlasse](general-electronic-reporting.md#Repository).

Selle teema näidetes on aktiivne pakkuja Contoso ja te kasutate seda malli loomiseks, mis põhineb Microsofti pakutaval mallil. Teise võimalusena saate malli luua oma malli Exceli vormingus üles laadides.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

[Äridokumendi haldusvideo](https://youtu.be/gAIYl-mM_pw) abil uue äridokumendi loomine (näidatud ülal) on kaasatud rakendusega saadaval olevasse [esitusloendisse](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)YouTube Finance and Operations.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Tee uus dokumendi kasutajaliides äridokumentide halduses kättesaadavaks

Et alustada uue dokumendi kasutajaliidese kasutamist äridokumentide halduses peate **Office'i sarnase kasutajaliidese kogemuse äridokumendi halduses** **Funktsiooni halduse** tööruumis sisse lülitama.

Kõigi juriidiliste isikute jaoks selle funktsiooni sisselülitamiseks toimige järgmiselt.

1. Valige **Fuktsioonide halduse** tööruumis vahekaardil **Kõik** loendis funktsioon **Office'i sarnase kasutajaliidese kogemus äridokumendi haldamises**.
2. Valitud funktsiooni lubamiseks valige **Luba kohe**.
3. Uue funktsiooni kasutamiseks värskenda lehte.

## <a name="add-or-activate-a-provider"></a>Teenusepakkuja lisamine või aktiveerimine

Iga äridokumendi mall talletatakse ER-vormingus konfiguratsioonis, mis on märgitud konkreetse konfiguratsioonipakkuja omandis olevaks. Uue malli loomisel luuakse selle hoidmiseks uus ER-vormingu konfiguratsioon. Seetõttu tuleb selle konfiguratsiooni jaoks tuvastada pakkuja. Selleks kasutatakse ER-i raamistiku aktiivset pakkujat. Kui ER-is pole teenusepakkujat, saate selle luua. Kui aktiivset *teenusepakkujat pole*, saate aktiveerida ühe olemasolevatest pakkujatest. Uue malli lisamise või aktiveerimise ajal avatakse dialoog teenusepakkuja lisamiseks või aktiveerimiseks, kui see on vajalik.

### <a name="add-a-new-provider"></a>Uue pakkuja lisamine

Uue pakkuja loomiseks tehke dialoogiboksis **Konfiguratsioonipakkuja** järgmist.

1.  Sisestage **menüü Konfiguratsioonipakkuja** valimine väljale **Nimi** uue pakkuja nimi.
2.  Sisestage **väljale Interneti-aadress** uue teenusepakkuja Interneti-aadress (URL). 
3.  Valige nupp **OK**.

    ![Uue pakkuja loomine äridokumentide halduses.](./media/bdm_create_provider.png)

Lisatud teenusepakkuja aktiveeritakse automaatselt.

### <a name="activate-a-provider"></a>Teenusepakkuja aktiveerimine

Teenusepakkuja aktiveerimiseks tehke dialoogiboksis **Konfiguratsioonipakkuja** järgmist.

1.  **Valige menüü Konfiguratsioonipakkuja** valimine väljal **Konfiguratsioonipakkuja** pakkuja.
2.  Valige nupp **OK**.

    ![Teenusepakkuja aktiveerimine äridokumendi halduses.](./media/bdm_choose_provider.png)

Valitud pakkuja aktiveeritakse.

> [!NOTE]
> Iga äridokumendi halduse mall asub ER-vormingus konfiguratsioonis, mis viitab pakkujale kui konfiguratsiooni autorile. Seetõttu on iga malli jaoks vaja aktiivset pakkujat.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Teisele pakkujale kuuluva malli redigeerimine

Selles näites **kirjeldatakse, kuidas kasutada** äridokumendi halduse **tööruumis nuppu Uus dokument** malli loomiseks ja redigeerimiseks ER-vormingus konfiguratsioonis, mille pakub mõni muu pakkuja ja mis asub praeguses finance'i eksemplaris. Selles näites on aktiivne pakkuja Contoso, mis kasutab Microsofti pakutavat ER-vormingu konfiguratsiooni. Pärast uue dokumendi **valimist** **kuvatakse lehe Uue malli** loomine vahekaardil Vali **kõik praeguse finance-eksemplari mallid, mis kuuluvad praegusele** pakkujale ja teistele pakkujatele. Valige selle avamiseks mall. Seejärel saate luua mallist uue redigeeritava koopia. Redigeeritud mall talletatakse uues ER-vormingus, mis luuakse automaatselt.

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.

    ![Äridokumentide halduse tööruum.](./media/BDM_overview_new_template1.png)

2. **Valige lehe** Uue malli **loomine menüü Vali** mallina kasutatav dokument ja seejärel valige **Loo dokument**.

    ![Äridokumentide dialoogiboks.](./media/BDM_overview_new_template2.png)

3. Muutke vajadusel pealkiri uue dialoogiboksi väljal **Pealkiri**. Pealkirja tekstiga nimetatakse ise tekkivat uut ER-vormingu seadistust. Seda muudetavat malli sisaldava seadistuse (**Kliendi FTI aruande (GER) koopia**) mustandit ja ER-vormingu praeguse kasutaja puhul. ER-vormingu põhiseadistuse muutmata algset malli kasutatakse selle ER-vormingu käivitamiseks kõikide kasutajate puhul.
4. Muutke väljal **Nimi** isetekkiva muudetava malli esimese redaktsiooni nime.
5. Väljal **Kommentaar** värskendage isetekkiva muudetava malli redaktsiooni märkusi.
6. Muutmis alustamise kinnitamiseks valige **OK**.

    ![Dokumendi loomise dialoogiboks.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Olemasolevat Exceli töövihikut kasutava malli üleslaadimine

Selles näites **kirjeldatakse, kuidas kasutada** äridokumendihalduse **tööruumis nuppu Uus dokument** malli loomiseks ja redigeerimiseks ER-vormingus konfiguratsioonis, mis põhineb saadaoleval Exceli töövihikul. Selles näites on aktiivne pakkuja Contoso ning kasutate Microsofti pakutavaid ER-andmemudeli [ja](er-overview-components.md#data-model-component) ER-mudeli [vastendamise](er-overview-components.md#model-mapping-component) konfiguratsioone. Pärast uue dokumendi **valimist** **valige lehel Uue malli** loomine vahekaart **Üleslaadimine**. Seal saate määrata Exceli töövihiku üleslaadimise üksikasjad. Pärast Exceli töövihiku üleslaadimist muudetakse see redigeerimiseks avatud äridokumendi malliks. Redigeeritud mall salvestatakse uude ER-vormingu konfiguratsiooni, mis luuakse automaatselt.

Enne malli üleslaadimist vajaliku teabe esitamiseks toimige järgmiselt.

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.
2. Klõpsake lehe **Uue malli loomine** vahekaardi **Üleslaadimine** vahekaardil **Mall** nuppu **Sirvi**, et leida ja valida Exceli fail, mida soovite mallina kasutada. Jaotises **Mall** täidetakse väljad **Pealkiri** ja **Kirjeldus** automaatselt. Nad määravad automaatselt loodava uue ER-vormingu konfiguratsiooni nime ja kirjelduse. Vajadusel saate neid välju redigeerida.
3. Määrake jaotise **Dokumendi liik** väljal **Nimi** äridokumendi liik. Seda väärtust kasutatakse õige andmeallika (st ER-mudeli konfiguratsiooni) otsimiseks.

    ![Vahekaart Mall lehe Loo uus mall vahekaardil Laadi üles.](./media/BDM_overview_new_UI_import_21.jpg)

4. Klõpsake menüü **Andmeallikas** kiirkaardil **Filter** nuppu **Rakenda filter**. Jaotises **Andmeallikas** täidetakse väli **Nimi** automaatselt või saate väärtuse käsitsi valida. Filtri abil saate otsida sobivat andmeallika nime nime, kirjelduse, riigi/regiooni tähise ja äridokumendi liigi alusel.

    ![Andmeallika vahekaart lehe Loo uus mall vahekaardil Laadi üles.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Kiirkaarti **Filter** kasutatakse õige andmeallika (st ER-mudeli konfiguratsiooni) otsimiseks. Üleslaaditava dokumendi jaoks sobivaima andmeallika leidmiseks saate redigeerida kõiki filtrivälju.
    > 
    > Kiirkaardi **Filter** tingimusi kasutatakse **OR**-tingimustena.

5. Valige vahekaardil **Vastendamine** käsk **Tuvasta automaatselt**. Väli **Ruudi definitsioon** täidetakse automaatselt või saate väärtuse käsitsi valida. Sellel vahekaardil kuvatakse malli ja mudeli elementide lõppvastendus.

    ![Uue malli loomine lehe üleslaadimise vahekaardil kaardistamine.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Jaotise **Malli struktuur** vastendamine kasutab andmeallika siltide või kirjelduste täielikku vastendust kasutaja keeles ja malli lahtrinimes.

6. Malli loomise kinnitamiseks ja redigeerimisprotsessi alustamiseks valige **Loo dokument**.

Lisateavet vt [Äridokumendi halduse ülevaatest](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Laadige mall globaalsest hoidlast üles

See näide näitab, kuidas kasutada **Uus dokument** nuppu **Äridokumentide haldamine** tööruum malli loomiseks ja redigeerimiseks ER-vormingus konfiguratsioonis, mille pakub Microsoft ja mis asub globaalses hoidlas. Selles näites on aktiivne pakkuja Contoso, mis kasutab Microsofti pakutavat ER-vormingu konfiguratsiooni. Pärast seda, kui olete valinud **Uus dokument**, **globaalsest hoidlast** vahekaarti **Looge uus mall** lehel kuvatakse kõik äridokumendi mallid, mis on salvestatud globaalsesse hoidlasse, kuid puuduvad praeguses Finance'i eksemplaris. Pärast malli valimist imporditakse see globaalsest hoidlast praegusesse Finance'i eksemplari, et luua uus redigeeritav koopia. Redigeeritud mall talletatakse uues ER-vormingus, mis luuakse automaatselt.

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.
2. peal **Looge uus mall** lehel **Import globaalsest hoidlast** vahekaarti, valige mallina kasutatav dokument ja seejärel valige **Loo dokument**.

    ![Importige lehe Loo uus mall vahekaardilt Globaalne hoidla.](./media/BDM_overview_new_template22.png)

3. Valige sõnumikastis **Jah** kinnitamaks, et soovite importida valitud dokumendi globaalsest hoidlast praegusesse Finance'i eksemplari. Kui teil palutakse autoriseerida, järgige ekraanil kuvatavaid juhiseid.
4. Muutke vajadusel pealkiri uue dialoogiboksi väljal **Pealkiri**. Pealkirja tekstiga nimetatakse ise tekkivat uut ER-vormingu seadistust. Selle konfiguratsiooni mustandversioon (**Inkassokirja märkus (Excel) Koopia**) sisaldab muudetud malli ja seda kasutatakse praeguse kasutaja jaoks selle ER-vormingu käitamiseks. ER-vormingu põhiseadistuse muutmata algset malli kasutatakse selle ER-vormingu käivitamiseks kõikide kasutajate puhul.
5. Muutke väljal **Nimi** isetekkiva muudetava malli esimese redaktsiooni nime.
6. Väljal **Kommentaar** värskendage isetekkiva muudetava malli redaktsiooni märkusi.
7. Muutmis alustamise kinnitamiseks valige **OK**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
