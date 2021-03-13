---
title: Kassa kasutajaliidese visuaalsed konfiguratsioonid
description: Selles teemas käsitletakse Dynamics 365 Commercei kassa ekraanipaigutusi.
author: boycezhu
manager: annbe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 203d12956825286b77a107bb9fd91c451ecfd1e6
ms.sourcegitcommit: dc3deca942864c4a8354096183c9e1b9b88992f6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/20/2021
ms.locfileid: "5032929"
---
# <a name="pos-user-interface-visual-configurations"></a>Kassa kasutajaliidese visuaalsed konfiguratsioonid

[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commerce'i kassa kasutajaliidest saab konfigureerida kauplustele, registritele ja/või kasutajatele määratud visuaalsete profiilide ja ekraanipaigutuste kombinatsiooni abil. Selles teemas antakse teavet nende konfiguratsioonisuvandite kohta.

Järgmine joonis näitab seoseid erinevate olemite vahel, millest kassa UI konfigureeritavad aspektid koosnevad.

![Kassa ekraanipaigutuse olemid](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Visuaalne profiil

Visuaalsed profiilid määratakse registritele ja need määravad kasutajate vahel jagatavad registripõhised visuaalsed elemendid. Iga kasutaja, kes registrisse sisse logib, näeb sama kujundust, paigutust, värve ja pilte.

![Kassa tervituskuva heleda kujundusega](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![Kassa kandekuva tumeda kujundusega](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profiili number** – profiili number on visuaalse profiili ainuidentifikaator.
- **Kirjeldus** – saate määrata kirjeldava nime, mis aitab tuvastada teie olukorra jaoks sobiva profiili.
- **Kujundus** – saate valida **heleda** või **tumeda** rakenduse kujunduse. Kujundus mõjutab kogu rakenduse fonti ja taustavärve.
- **Rõhuvärv** – rõhuvärvi kasutatakse kogu kassas teatud visuaalsete elementide (nt paanide, käsunuppude ja hüperlinkide) eristamiseks või esiletõstmiseks. Tavaliselt eeldavad need elemendid kasutajatoimingut.
- **Päise värv** – saate konfigureerida lehekülje päise värvi, et vastata jaemüüja kaubamärgi nõuetele.
- **Fondiskeem** – saate valida **standardsete** ja **suurte** fondiskeemide vahel. Fondiskeem mõjutab fondi suurust kogu rakenduses. Vaikevalik on **Standardne**.
- **Kuva alati rakenduse riba sildid** – kui see suvand on sisse lülitatud, kuvatakse sildi tekst alati rakenduse riba nuppude all.
- **Paigutus** – saate valida paigutuste **Keskel** ja **Paremal** vahel. Paigutus mõjutab sisselogimisvälja joondamist sisselogimisaknaga. Vaikevalik on **Keskel**.
- **Näita kuupäeva/kellaaega** – kui see valik on sisse lülitatud, kuvatakse see kuupäev ja kellaaeg Kassa päises ja sisselogimisaknas.
- **Klaviatuur** – saate teha valiku **Vaikimisi valik opsüsteemi klaviatuuri jaoks** või **Kuva numbriklahvistik**, et määrata vaikimisi klaviatuur, mida kasutatakse sisselogimisaknasse teksti sisestamiseks. Numbriklahvistik on virtuaalne klaviatuur, mida kasutatakse peamiselt puutetundlike seadmete jaoks. Vaikimisi valik on **Vaikimisi valik opsüsteemi klaviatuuri jaoks**.
- **Logo pilt** – saate määrata logo pildi, mis kuvatakse sisselogimisaknas. Soovitame kasutada läbipaistva taustaga pilti. Failid peaksid olema võimalikult väikesed, sest suurte failide talletamine ja laadimine võib mõjutada rakenduse toimimist ja jõudlust.
- **Sisselogimise taust** – saate määrata sisselogimisakna taustapildi. Taustapiltide failid peaksid olema võimalikult väikesed.
- **Taust** – saate määrata taustpildi, mida kasutatakse kogu rakenduses ühevärvilise kujunduse asemel. Sisselogimisakna taustapildid peaksid olema võimalikult väikesed.

> [!NOTE]
> Paigutus **Paremal** ja kuupäeva/kellaaja kuva ei rakendu kompaktses vaates sisselogimisaknale.

Peate käivitama jaotusgraafiku töö **1090** (**Registrid**), et sünkroonida uusimad visuaalse profiili konfiguratsioonid kanali andmebaasiga.

## <a name="screen-layouts"></a>Ekraani paigutused

Ekraanipaigutuse konfiguratsioonid määratlevad juhtelementide toimingud, sisu ja paigutuse kassa **tervitusekraanil** ning ekraanil **Kanne**.

![Kassa ekraanipaigutus](../commerce/media/POS-Screen-Layout-View.png)

- **Tervitusekraan** – enamasti on tervitusekraan leht, mida kasutajad näevad, kui nad alguses kassasse sisse logivad. Tervitusekraan võib koosneda kaubamärgipildist ja nupupaneelidest, millelt pääseb kassatoimingute juurde. Tavaliselt paigutatakse sellele ekraanile toimingud, mis ei ole jooksva kande põhised.

    ![Kassa tervitusekraan](../commerce/media/POS-Welcome-Screen.png)

- **Kandeekraan** – ekraan **Kanne** on kassa põhiekraan müügikannete ja tellimuste töötlemiseks. Sisu ja paigutust saab konfigureerida ekraani paigutuse kujundajaga.

    ![Kassa kandeekraan](../commerce/media/POS-Transaction-Screen.png)

- **Vaikeavakuva** – mõned jaemüüjad eelistavad, et kassapidajad läheksid pärast sisselogimist kohe ekraanile **Kanne**. Säte **Vaikeavakuva** võimaldab teil määrata vaikekuva, mis kuvatakse pärast sisselogimist iga ekraanipaigutuse korral.

### <a name="assignment"></a>Määramine

Ekraanipaigutusi saab määrata kaupluse, registri või kasutaja tasandil. Kasutaja määramine tühistab registri ja kaupluse määramised ning registri määramine tühistab kaupluse määramise. Lihtsas stsenaariumis, kus kõik kasutajad kasutavad sama paigutust, olenemata registrist või rollist, saab ekraanipaigutuse määrata ainult kaupluse tasemel. Kui teatud registrid või kasutajad nõuavad spetsiaalseid paigutusi, saab neid paigutusi määrata.

Sõltuvalt sellest, millisel tasemel on kuvapaigutused määratud, peate käivitama jaotusgraafiku töö **1070** (**Kanali konfiguratsioon**), **1090** (**Registrid**) ja/või **1060** (**Personal**), et sünkroonida uusimad kuvapaigutuse konfiguratsioonid kanali andmebaasiga.

### <a name="layout-sizes"></a>Paigutuse suurused

Kassa kasutajaliidese enamik aspekte on reageerivad ning paigutuse suurust muudetakse ja reguleeritakse automaatselt ekraani suuruse ja asetuse järgi. Kuid kassa ekraan **Kanne** tuleb konfigureerida iga soovitud ekraani eraldusvõime jaoks.

Käivitamisel valib kassarakendus automaatselt lähima paigutuse suuruse, mis on seadme jaoks konfigureeritud. Ekraani paigutus võib sisaldada ka konfiguratsioone horisontaal- ja vertikaalpaigutuse jaoks nii täissuuruses kui ka kompaktsete seadmete jaoks. Seetõttu saab kasutajatele määrata ühe ekraanipaigutuse, mis töötab kaupluse kasutatavate mitmesuguste suuruse ja vormi tegurite lõikes.

![Kassa paigutuse suurused](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Nimi** – saate ekraani suuruse tuvastamiseks sisestada tähendusliku nime.
- **Paigutuse tüüp** – kassarakenduse saab selle kasutajaliidese kuvada erinevates režiimides, et pakkuda igas seadmes parimat kasutuskogemust.

    - **Modern POS – täispaigutus** – täispaigutused sobivad tavaliselt kõige paremini suurematele ekraanidele, näiteks lauaarvuti kuvaritele ja tahvelarvutitele. Saate valida kasutatavaid kasutajaliidese elemente, määrata elementide suuruse ja paigutuse ning konfigureerida nende üksikasjalikke atribuute. Täispaigutused toetavad nii vertikaal- kui ka horisontaalkonfiguratsioone.
    - **Modern POS – kompaktne** – kompaktsed paigutused sobivad tavaliselt kõige paremini telefonidele ja väikestele tahvelarvutitele. Kompaktsete seadmete puhul on kujundusvõimalused piiratud. Saate konfigureerida sissetuleku ja kogusummade paneelide veerge ja välju.

- **Laius/kõrgus** – need väärtused tähistavad paigutuse jaoks eeldatud ekraani suurust pikslites. Pidage meeles, et mõned operatsioonisüsteemid kasutavad suure eraldusvõimega ekraanide jaoks mastaapimist.

> [!TIP]
> Kassa ekraani jaoks vajaliku paigutuse suuruse leiate, kui vaatate rakenduses eraldusvõimet. Käivitage kassa ja avage **Sätted \> Seansi teave**. Kassa kuvab praegu laaditud ekraani paigutuse, paigutuse suuruse ja rakenduse akna eraldusvõime.

![Kassa seansi teabe leht kuvab praegu laaditud ekraani paigutuse, paigutuse suuruse ja rakenduse akna eraldusvõime](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Nupupaneelid

Iga paigutuse suuruse korral ekraani paigutuses saate kassa tervituskuva ja ekraani **Kanne** jaoks konfigureerida ja määrata nupupaneele. Tervituskuva nupupaneelid paigutatakse automaatselt vasakult paremale, väikseimast numbrist (tervituskuva 1) suurima numbrini.

Kassa täispaigutustes on nupupaneelide paigutus määratletud ekraani paigutuse kujundajas.

Kassa kompaktsetes paigutustes paigutatakse nupupaneelid automaatselt ülevalt alla, väikseimast numbrist (kandekuva 1) suurima numbrini. Neile pääseb juurde menüüst **Tegevused**.

![Kompaktse paigutuse nupupaneelid](../commerce/media/Compact-View-Button-Grids.png)

> [!NOTE]
> Nupu suurused kujundajas sobituvad akna suurusega, seega ei pruugi nad tegelikke kassa nuppe täpselt peegeldada. Nupupaneeli paigutust saate kõige paremini simuleerida kohandades kujundaja akna sama suures, kui kassa.

### <a name="images"></a>Pildid

Saate iga paigutuse suuruse jaoks ekraani paigutuses määrata pildid, mis kaasata kassa kasutajaliideses. Kassa täispaigutuste korral saab tervituskuva jaoks määrata ühe pildi. See pilt kuvatakse kasutajaliidese esimese elemendina vasakul. Ekraanil **Kanne** saab pilte kasutada vahekaardi piltide või logona. Kompaktsetes kassa paigutustes ei kasutata neid pilte.

### <a name="screen-layout-designer"></a>Ekraani paigutuse kujundaja

Ekraanipaigutuse kujundaja võimaldab teil konfigureerida kassa ekraani **Kanne** erinevaid aspekte iga paigutuse suuruse jaoks nii horisontaal- kui ka vertikaalpaigutuses ja nii täissuuruses kui ka kompaktsete paigutuste korral. Ekraanipaigutuse kujundaja kasutab juurutuse tehnoloogiat ClickOnce rakenduse uusima versiooni allalaadimiseks, installimiseks ja käivitamiseks iga kord, kui kasutaja sellele juurde pääseb. Kontrollige brauseri nõudeid ClickOnce'i jaoks. Mõned brauserid, nagu Google Chrome, vajavad laiendusi.

> [!IMPORTANT]
> Peate konfigureerima ekraanipaigutuse iga paigutuse suuruse jaoks, mis on määratletud ja mida kassa kasutab.

### <a name="full-layout-designer"></a>Täispaigutuse kujundaja

Täispaigutuse kujundaja võimaldab kasutajatel lohistada kasutajaliidese juhtelemente ekraanile **Kanne** ja konfigureerida nende juhtelementide sätteid.

![Kassa täispaigutuse kujundaja (horisontaalrežiim)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Impordi paigutus / Ekspordi paigutus** – saate eksportida ja impordi kassa ekraanipaigutuse kujundusi XML-failidena, et saaksite neid erinevates keskkondades hõlpsalt uuesti kasutada ja ühiskasutusse anda. On oluline, et impordite paigutuse kujundused õigete paigutuse suuruste jaoks. Vastasel juhul ei pruugi kasutajaliidese elemendid õigesti ekraanile sobida.
- **Horisontaalne/vertikaalne režiim** – kui kassaseade võimaldab kasutajatel vahetada horisontaalse ja vertikaalse režiimi vahel, peate iga režiimi jaoks määratlema ekraanipaigutuse. Kassa tuvastab ekraani pööramise automaatselt ja kuvab õige paigutuse.
- **Paigutuse ruudustik** – kassa paigutuse kujundaja kasutab nelja piksliga ruudustikku. Kasutajaliides kontrollib ruudustikku „tõmbamist”, et aidata teil sisu õigesti joondada.
- **Kujundaja suum** – saate suumida kujundaja vaadet sisse ja välja, et näha sisu kassaekraanil paremini. See funktsioon on kasulik, kui kassaekraani eraldusvõime erineb oluliselt kujundajas kasutatava ekraani eraldusvõimest.
- **Navigeerimisriba kuvamine/peitmine** – kassa täispaigutuste jaoks saate valida, kas ekraanil **Kanne** on vasakpoole navigeerimisriba nähtav. See funktsioon on kasulik väiksema eraldusvõimega ekraanidel. Nähtavuse seadmiseks paremklõpsake kujundajas navigeerimisribal ja märkige või tühjendage märkeruut **Alati nähtav**. Kui navigeerimisriba on peidetud, saavad kassa kasutajad sellele siiski juurdepääsu üleval vasakul oleva menüü abil.

    ![Kuva/peida navigeerimisriba](../commerce/media/Navigation-Bar.PNG)

- **Kassa juhtelemendid** – kassa paigutuse kujundaja toetab järgmisi juhtelemente. Saate paljusid juhtelemente konfigureerida paremklõpsates ja kasutades kiirmenüüd.

    ![Kassa kasutajaliidese juhtelemendid](../commerce/media/POS-UI-Controls.png)

    - **Numbriklahvistik** – numbriklahvistik on kassa ekraanil **Kanne** peamine kasutaja sisestusvahend. Saate konfigureerida juhtelemente nii, et kuvatakse kogu numbriklahvistik. See valik sobib hästi puuteekraaniga seadme korral. Teise võimalusena saate seda konfigureerida nii, et kuvatakse ainult sisestusväli. Sellisel juhul kasutatakse sisestamiseks füüsilist klaviatuuri. Numbriklahvistiku sätted on saadaval ainult täispaigutuses. Kompaktsete paigutuste korral kuvatakse ekraanil **Kanne** alati kogu numbriklahvistik.
    - **Kogusummade paneel** – saate konfigureerida kogusummade paneeli ühes või kahes veerus kuvama väärtusi, nagu ridade arv, allahindluse summa, tasud, vahesumma ja maksud. Kompaktsed paigutused toetavad ainult üht veergu.
    - **Sissetuleku paan** – sissetuleku paan sisaldab müügiridu, makseridu ja tarneteavet kassas töödeldavate toodete ning teenuste kohta. Saate määrata veerge, laiusi ja paigutust. Kompaktsetes paigutustes saate konfigureerida ka lisateavet, mis kuvatakse real põhirea all.
    - **Kliendikaart** – kliendikaart näitab praegu kandega seotud kliendi andmeid. Saate kliendikaardi konfigureerida lisateavet peitma või kuvama.
    - **Vahekaardi juhtelement** – saate ekraanipaigutuse peale lisada vahekaardi juhtelemendi ja seejärel paigutada vahekaardi sisse teisi juhtelemente (nt numbriklahvistiku, kliendikaardi või nupupaneelid). Vahekaardi juhtelement on konteiner, mis aitab teil ekraanile rohkem sisu paigutada. Vahekaardi juhtelement on saadaval ainult täispaigutuste puhul.
    - **Pilt** – saate kasutada pildi juhtelementi kaupluse logo või muu tootjakohanduse teabe kuvamiseks ekraanil **Kanne**. Pildi juhtelement on saadaval ainult täispaigutuste puhul.
    - **Soovitatud tooted** – kui soovitatud toodete juhtelement on keskkonna jaoks konfigureeritud, näitab see masinõppel põhinevaid tootesoovitusi.
    - **Kohandatud juhtelement**– kohandatud juhtelement toimib ekraanipaigutuses kohatäitena ja võimaldab teil kohandatud sisu jaoks ruumi reserveerida. Kohandatud juhtelement on saadaval ainult täispaigutuste puhul.

### <a name="compact-layout-designer"></a>Kompaktse paigutuse kujundaja

Kompaktse paigutuse kujundaja võimaldab teil sarnaselt täispaigutuse kujundajale konfigureerida kassaekraani paigutust telefonide ja väikeste tahvelarvutite jaoks. Kuid sellisel juhul on paigutus fikseeritud. Saate paigutuse juhtelemente konfigureerida paremklõpsates ja kasutades kiirmenüüd. Kuid te ei saa täiendavat sisu hiirega pukseerida.

![Kompaktse paigutuse kujundaja](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Nupupaneeli kujundaja

Nupupaneeli kujundaja võimaldab teil konfigureerida nupupaneele, mida kasutatakse nii täis- kui ka kompaktses paigutuses kassa tervituskuval ja ekraanil **Kanne**. Sama nupupaneeli saab kasutada kõigis paigutustes ja paigutuse tüüpides. Nupupaneeli kujundaja kasutab sarnaselt ekraanipaigutuse kujundajale juurutuse tehnoloogiat ClickOnce rakenduse uusima versiooni allalaadimiseks, installimiseks ja käivitamiseks iga kord, kui kasutaja sellele juurde pääseb. Kontrollige brauseri nõudeid ClickOnce'i jaoks. Mõned brauserid, nagu Google Chrome, vajavad laiendusi.

![Nupupaneeli kujundaja](../commerce/media/Button-Grid-Designer.png)

- **Uus nupp** – klõpsake uue nupu lisamiseks nupupaneelile. Vaikimisi kuvatakse uued nupud paneeli ülemises vasakpoolses nurgas. Kuid saate nuppe neid paigutuses lohistades ümber paigutada.

    > [!IMPORTANT]
    > Nupupaneeli sisu saab kattuda. Kui paigutate nuppe ümber, veenduge, et need ei peidaks teisi nuppe.

- **Uus kujundus** – klõpsake nupupaneeli paigutuse automaatseks seadistamiseks, määratledes nuppude arvu rea ja veeru kohta.
- **Nupu atribuudid** – saate konfigureerida nupu atribuute, paremklõpsates nupul ja kasutades kiirmenüüd.

    > [!IMPORTANT]
    > Mõned nupupaneeli sätted kehtivad ainult ettevõtte kassas, mitte Modern POS-is ega pilvekassas.

    ![Nupupaneeli nupu atribuudid](../commerce/media/Button-grid-button-properties.png)

    - **Tegevus** – valige kohaldatavate kassatoimingute loendist toiming, mis käivitatakse nupu klõpsamisel kassas.

        Toetatud kassatoimingute loendi leiate jaotisest [Ühendusega ja ühenduseta kassatoimingud](pos-operations.md).

    - **Toimingu parameetrid** – mõned kassatoimingud kasutavad nende käivitamisel täiendavaid parameetreid. Näiteks saavad kasutajad toimingu Lisa toode jaoks määrata lisatava toote.
    - **Nupu tekst** – saate määrata teksti, mis kuvatakse kassas nupul.
    - **Peida nupu tekst** – kasutage seda märkeruutu nupu teksti peitmiseks või kuvamiseks. Nupu tekst on sageli peidetud väikeste nuppude korral, mille jaoks kuvatakse ainult ikoon.
    - **Kohtspikker** – saate määratava täiendava spikri teksti, mis kuvatakse, kui kasutaja viib hiire nupu kohale.
    - **Suurus veergudes / suurus ridades** – saate määrata, kui kõrge ja lai nupp on.

        ![Kassa nuppude suurused ridades ja veergudes](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Kohandatud font** – kui valite märkeruudu **Luba kassa jaoks kohandatud font**, saate valida muu fondi kui kassa süsteemi vaikefont.
    - **Kohandatud kujundus** – vaikimisi kasutatakse kassa nuppude jaoks rõhuvärvi visuaalsest profiilist. Kui valite märkeruudu **Kasuta kohandatud kujundust**, saate määrata täiendavad värvid.

        > [!NOTE]
        > Modern POS ja pilvekassa kasutavad ainult väärtusi **Taustavärv** ja **Fondi värv**.

    - **Nupu pilt** – nuppudele saab lisada pilte või ikoone. Valige saadaolevate piltide hulgast, mis on toodud asukohas **Jaemüük ja kaubandus \> Kanali häälestus \> Kassa häälestus \> Kassa \> Pildid**.

![Nupupaneeli näide kassas](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Lisaressursid

[Jaemüügikassa paigutuse kujundaja installimine](install-pos-layout-designer.md)
