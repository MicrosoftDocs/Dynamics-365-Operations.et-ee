---
title: Kasutuskogemuse isikupärastamine
description: Selles teemas selgitatakse, kuidas isikupärastada rakendust.
author: jasongre
manager: AnnBe
ms.date: 06/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edf698b12f2d0bcb6035bc644537cf9ca2bb87c9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190898"
---
# <a name="personalize-the-user-experience"></a>Kasutuskogemuse isikupärastamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas isikupärastada rakendust.

Isikupärastamise põhiklasse on kolm.

- Isikupärastamine on võimalik seadistuslehel. Näiteks võib tuua värvikujunduse ja ajavööndi.
- Lehekasutusega seotud isikupärastamised ehk *varjatud* isikupärastamised. Näiteks jälgib süsteem ruudustiku veerulaiusi, kui neid korrigeerite, ja kiirkaartide laiendatud või ahendatud olekut.
- Isikupärastamised, mille kasutaja teeb lehe välimuse muutmiseks, muutes elemendi lehel ilmumise või toimimise viisi, sageli interaktiivse isikupärastamisrežiimi kaudu. Neid isikupärastamisi nimetatakse *varjatud* isikupärastamiseks. Näiteks võib kasutaja lehele elemente lisada, neid peita või ümber järjestada.

Kõik isikupärastamised, mille kasutaja teeb, on ainult sellele kasutajale olenemata isikupärastamise tüübist või ettevõttest, millega kasutaja parajasti suhtleb. Ühe kasutaja lehele tehtud muudatused ei mõjuta süsteemi teisi kasutajaid.

## <a name="system-wide-options-for-the-current-user"></a>Süsteemiülesed suvandid praegusele kasutajale

Leht **Kasutaja suvandid** sisaldab mitut süsteemiülest sätet praegusele kasutajale. Lehe **Kasutaja suvandid** avamiseks valige navigeerimisribal menüü **Sätted** (hammasrattaikoon) ja siis valige **Kasutaja suvandid**. Lehel **Kasutaja suvandid** on neli vahekaarti erinevate kasutajasätetega.

- **Visuaalne** – saate valida lehtede värvikujunduse ja elementide vaikesuurused.
- **Eelistused** – saate valida vaikeväärtused, mida kasutatakse iga kord, kui süsteemi avate. Väärtused hõlmavad ettevõtet, avalehte ja kuvamise/redigeerimise vaikerežiimi. (Kuva-/redigeerimisrežiim määrab, kas leht on vaatamiseks lukus või avaneb iga kord redigeerimiseks, kui selle avate.) Sellel vahekaardil on ka suvandid keele, ajavööndi ning kuupäeva-, kellaaja- ja numbrivormingu valimiseks. Samuti sisaldab see vahekaart mitmesuguseid eelistusi, mis erinevad olenevalt väljaandest.
- **Konto** – saate kohandada oma kasutajanime ja muid kontoga seotud suvandeid.
- **Töövoog** – saate valida seotud suvandeid.

Lisaks kasutajasätete muutmisele saate vaadata ja kustutada ka oma kasutusandmed ning isikupärastamisi, klõpsates nuppu **Kasutusandmed**. Rakenduse kasutamisel salvestatakse paljud teie valikud, et muuta süsteemi kasutamine tulevikus teie jaoks lihtsamaks. Süsteemi lehtedele tehtud isiklikke muudatusi võimaldab teil vaadata ja hallata eelkõige vahekaart **Isikupärastamine**. Sellel vahekaardil on võimalik lähtestada ka funktsioonide viiktekste ehk hüpikaknaid, mis tutvustavad teile süsteemi uusi funktsioone (saadaval platvormivärskenduses 26) nii, et teid teavitatakse uuesti funktsioonidest, millega te olete varem juba kokku puutunud.  

## <a name="implicit-personalizations"></a>Varjatud isikupärastamised

Varjatud isikupärastamised on need isikupärastamised, mida teete teatud juhtnuppe reguleerides, mis jätavad oma praeguse nähtava oleku meelde.

- **Ruudustiku veerud** – saate korrigeerida veeru laiust ruudustikus, valides veerupäisest vasakul või paremal oleva suuruse muutise riba ja libistades seda vasakule või paremale, kuni veerg on soovitud laiusega. Rakendus salvestab veeru jaoks valitud laiuse. Seejärel muudab see veeru laiuse valitud sättele iga kord, kui avate lehe, mis seda ruudustikku sisaldab.
- **Kiirkaardid** – mõnel lehel on laiendatavad jaotised, mida nimetatakse *kiirkaartideks*. Rakendus salvestab kiirkaartide laiendamise ja ahendamise teabe. Seejärel laiendatakse või ahendatakse samad kiirkaardid iga kord, kui lehele naasete, võttes aluseks teie viimase tegevuse lehel. Mõnel juhul saate kiirkaardi ahendamisega aidata süsteemi jõudlust parandada, sest rakendus ei pea selle kiirkaardi teavet tooma, kuni kiirkaarti ei laiendata. Nagu hiljem selles teemas on selgitatud, saate muuta ka kiirkaartide järjestust lehel.
- **Kiirinfo** – mõnel lehel on jaotis, mida nimetatakse *kiirinfo paaniks*. See paan sisaldab kirjutuskaitstud teavet, mis on seotud lehe praeguse teemaga. Igat kiirinfo paani jaotist nimetatakse *kiirinfoks*. Saate kogu kiirinfo paani peita või kuvada, samuti laiendada või ahendada üksikuid kiirinfosid. Rakendus salvestab teie eelistused. Seejärel taastatakse kiirinfo paani ja üksikute kiirinfode olek iga kord, kui lehele naasete, võttes aluseks teie viimase tegevuse lehel. Mõnel juhul saate kiirinfo ahendamisega aidata süsteemi jõudlust parandada, sest rakendus ei pea selle kiirinfo teavet tooma, kuni kiirinfot ei laiendata.
- **Toimingupaanid** – *toimingupaan* kuvatakse enamiku lehtede ülaserva lähedal. Toimingupaan sisaldab nuppe paljudeks tegevusteks, mida praegusel lehel saate teha. Need nupud on sageli korraldatud vahekaartidele. Saate kogu toimingupaani kinnitada avatuna või hoida selle vaikimisi ahendatuna. Seejärel taastab rakendus toimingupaani kinnitatud oleku, kui lehe järgmine kord avate. Kui toimingupaan on avatuna kinnitatud, kuvab rakendus ka teie viimati kasutatud tegevuste vahekaardi.
- **Kiirfiltrid** – *kiirfilter* kuvatakse paljude ruudustike kohal. Kiirfiltriga saate ruudustikku filtreerida valitud veeru põhjal. Rakendus salvestab filtreeritud veeru valiku. Seejärel filtreeritakse ruudustik sama veeru järgi, kui seda ruudustikku sisaldava lehe järgmine kord avate. Siiski on teil võimalik ruudustikku seejärel teise veeru alusel filtreerida.
- **Veerupäisefiltrid** – kui filtreerite ruudustiku *veerupäisefiltritega*, saate soovitud andmete leidmiseks muuta filtri operaatorit soovitud viisil. Näiteks saate valida tehtemärgi **algab väärtusega** asemel tehtemärgi **on täpselt**. Iga kord, kui kasutate veerupäisefiltrit ja muudate filtri tehtemärki, salvestab rakendus muudatuse. Seejärel taastab see filtri tehtemärgi järgmine kord, kui selle veeru alusel filtreerite.
- **Navigeerimispaan** – saate avada *navigeerimispaani*, valides mis tahes lehe vasakul paanil nupu **Menüü**. (Nuppu **Menüü** nimetatakse mõnikord *hamburgeriks*, *hamburgerimenüüks* või *hamburgerinupuks*.) Saate kinnitada navigeerimispaani avatuna või hoida selle vaikimisi ahendatuna. Kui olete navigeerimispaani avatuna kinnitanud, hoiab rakendus seda lahti, kuni selle ahendate.

## <a name="explicit-personalizations"></a>Selged isikupärastamised

Erinevad inimesed ja ettevõtted näevad erineval moel andmeid, mis on nende jaoks olulisimad või mis ei käitu viisil, nagu neil oma äri käitamiseks on vaja. Saate kohandada oma teabe korralduse ja sellega suhtlemise viisi. Saate ka määrata, et osa teabest peab olema peidetud. Need võimalused on aluseks isiklikule ja tulemuslikule kogemusele ning on näited sõnaselgetest isikupärastamistest. Selged isikupärastamised on isikupärastamised, mille teete selge kavatsusega muuta elemendi või lehe välimust või käitumist muuta.

### <a name="shortcut-menu-options"></a>Otseteemenüü suvandid

Otseteemenüüd pakuvad mitut võimalust lehe selgeks muutmiseks, et see sobiks paremini teie enda või teie ettevõtte nõuetega. (Otseteemenüüd nimetatakse ka *paremklõpsuga avatavaks menüüks* või *kontekstimenüüks*.)

Mõned tüüpilisimad ja olulisimad muudatused, mille lehele saab teha, on saadaval otse, kasutades otseteemenüü suvandeid. Näiteks kui soovite alates platvormivärskendusest 17 lisada ruudustikku veerge või neid peita, lihtsalt paremklõpsake ruudustiku veerupäisel ja siis valige käsk **Lisa veerge** või **Peida see veerg**.

Peale selle on enamik selge isikupärastamise tüüpe saadaval, kui paremklõpsate elemendil ja valite käsu **Isikupärastamine**. (Arvestage sellega, et kõiki lehel olevaid elemente ei saa isikupärastada.) Kui valite selle isikupärastamise viisi, ilmub elemendi atribuudiaken.

![Elemendi atribuutide isikupärastamine](./media/personalization-element-properties.png)

Atribuudiakna kaudu on elemendi isikupärastamiseks järgmised võimalused.

- Elemendi sildi muutmine.
- Elemendi peitmine, nii et seda lehel ei kuvata. Väljal olevaid andmeid ei kustutata ega muudeta. Lihtsalt lehel ei kuvata enam teavet.
- Teabe lisamine kiirkaardi kokkuvõttejaotisse (kui element on kiirkaardil).
- Välja vahelejätmine, kui vajutate tabulaatoriklahvi lehel olevate väljade vahel liikumiseks.
- Väljal olevate andmete (mis tahes kirje puhul) redigeerimise takistamine.

Atribuudiaken võib sisaldada ka muid isikupärastamisvõimalusi olenevalt elemendist. Näiteks paani atribuudiaken võib lubada teil ülendada selle paani armatuurlauaks ja armatuurlaua atribuudiaken võib lubada teil luua sellel armatuurlaual uue tööruumi.

### <a name="the-personalization-toolbar"></a>Isikupärastamise tööriistariba

Kui soovite teha lehele mitu muudatust või teete muudatusi, mis pole muude mehhanismide (nt elementide ümberjärjestamine) kaudu saadaval, saate kasutada tööriistariba **Isikupärastamine**. Tööriistariba **Isikupärastamine** avamiseks valige elemendi atribuudiaknas suvand **Selle vormi isikupärastamine**. Saate valida suvandi **Selle vormi isikupärastamine** iga lehe toimingupaani vahekaardil **Suvandid** olevast rühmast **Isikupärastamine**.

[![Isikupärastamise tööriistariba](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Lehel liikumine

Võimalus liikuda lehel, kui **Isikupärastamise tööriistariba** on avatud, sõltub kasutatavast platvormi versioonist.

- Enne platvormivärskendust 19, on leht, kui tööriistariba **Isikupärastamine** on avatud, kirjutuskaitstud (midagi ei saa sisestada) ja mitteinteraktiivne (muuta saab ainult lehe nähtavaid elemente). Kui soovite muuta ahendatud jaotises või teisel vahekaardil olevaid elemente, peate tööriistariba **Isikupärastamine** sulgema, jaotise laiendama või soovitud vahekaardile lülituma ja seejärel vahekaardi **Isikupärastamine** uuesti avama.

- Alates platvormivärskendusest 19 on leht, kui tööriistariba **Isikupärastamine** avatud, endiselt kirjutuskaitstud, kuid interaktiivsem. Täpsemalt saate kiirinfopaani laiendada või ahendada, vahekaartidel liikuda ja jaotisi laiendada või ahendada, kui tööriistariba **Isikupärastamine** on avatud, samamoodi, nagu seda tavaliselt lehel teete. Isikupärastamismuudatuse rakendamiseks ahendatavale jaotisele või vahekaardile (nt kiirkaardi peitmine), käivitate ahendatava jaotise või vahekaardi kõrval kuvatava nupu, kui sellele klaviatuuri või hiire abil liigute.

#### <a name="personalization-tools"></a>Isikupärastamise tööriistad

Tööriistaribal **Isikupärastamine** on saadaval järgmised tööriistad.

- Tööriistaga **Vali** saate valida ja muuta elemendi atribuute. Valige tööriist **Vali** ja seejärel element, mille atribuute soovite muuta. Elemendi valimisel avaneb elemendi atribuudiaken ja te saate muuta selle elemendi mis tahes atribuute. Saate protsessi selle lehe muude isikupärastatavate elementide puhul korrata. Olenevalt aga mõne elemendi kasutusviisist ei lase rakendus teil kõiki selle atribuute muuta. Seetõttu võite elemendi valimisel näha, et mõnd selle atribuuti ei saa muuta. Näiteks ei saa te vajalikku välja peita.
- Tööriistaga **Teisalda** saate nihutada elemendi praeguses elemendirühmas teise asukohta. (Elementi ei saa teisaldada emagrupist väljapoole). Valige tööriist **Teisalda** ja siis valige teisaldatav element. Elemendi valimisel kontrollib rakendus lehte, et teha kindlaks, kuhu elemendi saab teisaldada. Seejärel loob see pukseerimistsoonide loetelu. Elemendi lohistamisel praeguses rühmas kuvatakse iga pukseerimistsoon värvilisena ja paksu joonega selle ala kõrval, kuhu elemendi saab pukseerida.
- Tööriistaga **Peida** saate elemendi lehel peita. Valige tööriist **Peida** ja siis valige peidetav element. Tööriista **Peida** valimisel muudetakse kõik parasjagu peidetud elemendid nähtavaks ja kuvatakse varjutatud konteineris. Seejärel saate need nähtavale tuua. Valides tööriista **Vali**, saate vaadata, milline näeb leht välja, kui valitud elemendid on peidetud.

    - Alates platvormivärskendusest 18 saate vajalikud väljad ja vajalikke välju sisaldavad jaotised peita. See võimaldab hõlbustada kasutusviisi, kus äriloogikaga vaikimisi täidetud välju ei kuvata. Peidetud väljad saab ka ajutiselt nähtavaks teha, kui need on salvestamisel tühjad.

- Tööriistaga **Kokkuvõte** saate kuvada elemendi kiirkaardi kokkuvõttejaotises. Tööriist Kokkuvõte rakendub ainult väljadele, mis sisalduvad kiirkaardi jaotises. Tööriista **Kokkuvõte** valimisel kuvatakse kõik kokkuvõtteväljadena valitud väljad varjutatud konteineris. Saate välju interaktiivselt kiirkaardi kokkuvõttesse lisada ja neid sealt eemaldada, valides soovitud väljad.
- Tööriistaga **Jäta vahele** saate eemaldada elemendi lehe klaviatuuri vahekaardijärjestusest. Tööriista **Jäta vahele** valimisel kuvatakse kõik parasjagu vahelejäetud elemendid varjutatud konteineris. Seejärel saate need muuta uuesti vahekaardijärjestuse osaks.
- Tööriistaga **Redigeeri** saate märkida elemendi redigeeritavaks või mitteredigeeritavaks. Tööriista **Redigeeri** valimisel kuvatakse kõik parasjagu mitteredigeeritavad elemendid varjutatud konteineris. Seejärel saate need uuesti redigeeritavaks muuta. Arvestage sellega, et mõned väljad on nõutavad ja neid ei saa mitteredigeeritavaks muuta. Nende väljade kõrval kuvatakse tabalukuikoon.
- Nupuga **Sisesta** saate kuvada loendi elementidest, mida saab lehele lisada.

    - Lehele välja lisamiseks valige nupu **Sisesta** alt tööriist **Väli**. Tööriista **Väli** kasutamisel saate lisada ainult välju, mis on osa lehe määratlusest, kuid mida praegu lehel ei kuvata. Teavet selle kohta, kuidas luua uusi välju, mis ei ole osa praeguse lehe määratlusest, vt jaotisest [Kohandatud väljad](user-defined-fields.md). Tööriista **Väli** valimisel peate esmalt valima rühma või ala, kuhu soovite välja lisada. Dialoogiboksis kuvatakse valitud rühma või alaga seotud väljade loend. Valige dialoogiboksis lisamiseks üks või mitu välja ja seejärel valige käsk **Sisesta**. Varem lisatud välja eemaldamiseks korrake protsessi, kuid tühjendage dialoogiboksis välja valik.
    - Microsoft PowerAppsiga loodud rakenduse manustamiseks lehele valige suvandis **Sisesta** tööriist **PowerApp**. Üksikasjalikku teavet lehele PowerAppsi rakenduse manustamise kohta vt jaotisest [PowerAppsi manustamine](embed-power-apps.md).

- Valige nupp **Halda**, et kuvada praeguse lehe kõigi isikupärastamistega seotud haldamissuvandite loend.

    - Valige suvand **Eemalda** lehe lähtestamiseks vaikesätetele, installitud olekusse. Kõik praeguse lehe isikupärastamised eemaldatakse. Tagasivõtmine ei ole võimalik. Seetõttu kasutage seda suvandit ainult siis, kui soovite lehe lähtestada.
    - Suvandiga **Impordi** saadida laadida isikupärastamise failist, mille teie või keegi teine on lehe jaoks varem loonud. Kõik teie praegused lehe isikupärastamised asendatakse isikupärastamistega valitud failist.
    - Suvandiga **Ekspordi** saate oma lehe isikupärastamised failina salvestada. Saate oma isikupärastamisi teiste kasutajatega jagada. Need kasutajad peavad lihtsalt importima teie lehe isikupärastamisi sisaldava faili.

- Valige nupp **Sule**, kui soovite tööriistariba **Isikupärastamine** sulgeda ja lehe eelmise interaktiivse oleku taastada.

Tööriistariba **Isikupärastamine** kasutamisel toimub salvestamine varjatult. Teie isikupärastamised jõustuvad kohe, kui need teete, ja teil pole vaja valida nuppu **Salvesta**. Mõnel juhul kuvatakse tööriista valimisel elemendi kõrval tabalukuikoon. See ikoon näitab, et valitud tööriistaga seotud elemendi atribuute ei saa muuta, kuna nende atribuutide muutmine takistab lehe korralikku toimimist.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Tööruumile paani, loendi või lingi lisamine

Mõne loendeid sisaldava lehe puhul on saadaval täiendav isikupärastamisfunktsioon. Toimingupaani vahekaardi **Suvandid** rühmas **Isikupärastamine** olev nupp **Lisa tööruumi** võimaldab kuvada praegusest loendist pärit teabe kindlas tööruumis. Saate kuvada teavet tööruumis sorditud ja filtreeritud kujul või kuvada vaikevaate. Samuti saate määrata, kas teave kuvatakse tööruumis loendina, kokkuvõttepaanina, mis võib näidata loendis olevate üksuste arvu, või lingina.

[![Lisa tööruumi](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Tööruumile loendi lisamiseks tööruumi sortige või filtreerige esmalt lehel loend, et see kuvaks teavet nii, nagu soovite seda tööruumis kuvada. Seejärel valige suvand **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Loend**. Pärast suvandi **Konfigureeri** valimist ilmub dialoogiboks, kus saate valida veerud, mis peaks tööruumis loendis ilmuma. Saate ka määrata tööruumis olevale loendile sildi.
- Tööruumile paani lisamiseks filtreerige esmalt lehel loendit, et see kuvaks andmed, mida soovite kokku võtta või millele soovite kiiret juurdepääsu. Seejärel valige suvand **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Paan**. Kui olete valinud suvandi **Konfigureeri**, ilmub dialoogiboks, kus saate määrata tööruumis olevale paanile sildi. Saate ka määrata, kas paanil kuvatakse arv. Kui paan on tööruumi lisatud, saate selle valida, et avada praegune leht tööruumist ja kuvada paaniga seostatud filtreeritud loend.
- Tööruumile lingi lisamiseks filtreerige esmalt lehel loend, nii et see kuvaks andmeid, millest olete huvitatud. Seejärel valige suvand **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Link**. Kui olete valinud suvandi **Konfigureeri**, ilmub dialoogiboks, kus saate määrata tööruumis olevale lingile sildi. Samuti saate määrata sildi uuele jaotisele, mis seda linki sisaldab.

Kui loend, paan või link on tööruumile lisatud, saate tööruumi avada ja elemendid soovitud viisil ümber järjestada.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Kokkuvõtte lisamine tööruumist armatuurlauale

Mõni tööruum sisaldab arvpaane (st paane, millel on arvud) ja teil on võimalik ka need paanid armatuurlaual kuvada. Paremklõpsake tööruumis arvpaani ja valige suvand **Isikupärasta**. Seejärel valige paani atribuudiaknas suvand **Kinnita armatuurlauale**. Järgmine kord, kui te valitud armatuurlaua avate, kuvatakse arv selle tööruumi navigeerimispaani all. Saate suunata selle arvu otse asjassepuutuvate andmete juurde.

### <a name="personalizing-your-dashboard"></a>Armatuurlaua isikupärastamine

Armatuurlaud on tihti esimene leht, mida näete rakenduse avamisel. Saate armatuurlaua isikupärastada, nii et sellel kuvatakse ainult need tööruumi paanid, mida soovite näha. Saate paane ka ümber korraldada soovitud järjestusse, tööruumi navigeerimispaanid ümber nimetada või lisada täiesti uusi tööruumi paane.

Armatuurlaua isikupärastamiseks lihtsalt paremklõpsake mis tahes paanil ja valige suvand **Isikupärastamine**, et avada paani atribuudiaken.

- Kui soovite valitud paani peita või ümber nimetada, saate muudatuse teha otse atribuudiaknas.
- Tööruumi paanide ümberjärjestamiseks valige atribuudiaknas suvand **Selle vormi isikupärastamine**, et avada tööriistariba **Isikupärastamine**. Seejärel saate kasutada paanide soovitud viisil ümberkorraldamiseks tööriista **Teisalda**.
- Uue tööruumipaani loomiseks valige atribuudiaknas käsk **Lisa tööruum**. Uus tööruumipaan luuakse armatuurlaua alaserva. Saate selle uue tööruumipaani soovitud viisil ümber nimetada. Samuti lisada tööruumi loendeid, paane ja linke, nagu on kirjeldatud selle teema jaotises [Tööruumidesse loendite, paanide või linkide lisamine](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace).

## <a name="administration-of-personalization"></a>Isikupärastamise haldamine

Pärast lehe isikupärastamist võite oma isikupärastamisi oma isikupärastatud lehe eksportimise teel teiste kasutajatega jagada. Seejärel võite paluda teistel kasutajatel avada isikupärastatud leht ja importida teie loodud isikupärastamise fail. Teine võimalus on anda oma isikupärastamine administraatoriõigustega kasutajale. See kasutaja saab seejärel rakendada teie isikupärastamisfaili korraga paljudele kasutajatele.

Administraatori õigustega kasutaja saab lehel **Isikupärastamine** hallata ka teiste kasutajate isikupärastamisi. Sellel lehel on neli menüüd.

- **Rakenda** – saate importida või valida vähemalt ühe kasutaja isikupärastamise. Isikupärastamise rakendamiseks ühele või mitmele kasutajale valige esmalt roll ja selle rolliga kasutajad. Seejärel valige kas olemasolev isikupärastamine valitud kasutajatele rakendamiseks või importige isikupärastamise fail. Isikupärastamine kinnitatakse ja rakendatakse valitud kasutajatele järgmisel korral, kui nad valitud lehe avavad.
- **Eemalda** – saate eemaldada vähemalt ühe kasutaja lehe või tööruumi kõik isikupärastamised. Esmalt valige leht või tööruum, et näha seda isikupärastanud kasutajate loendit. Seejärel valige kasutajad, kelle isikupärastamised tuleb sellelt lehelt või sellest tööruumist eemaldada, ja valige käsk **Eemalda**. Kõik isikupärastamised, mille valitud kasutajad on valitud lehele või tööruumile rakendanud, kustutatakse. Seda tegevust ei saa tagasi võtta. Kui aga isikupärastamine on lehele või tööruumile salvestatud, saab selle isikupärastamise uuesti importida.
- **Haldur kasutaja kohta** – saate valida kasutaja, et kuvada loend lehtedest, mille kasutaja on isikupärastanud. Seejärel saate lubada või keelata valitud kasutaja võimaluse kasutada isikupärastamisi kindlatel lehtedel või terves süsteemis. Samuti saate valitud kasutaja jaoks isikupärastamise importida, eksportida või eemaldada. Peale selle saate valitud kasutaja puhul lähtestada funktsioonide viiktekste, millega kuvatakse varem kõrvale jäetud hüpikaknaid, mis tutvustasid uusi funktsioone, uuesti järgmine kord, kui kasutaja nende funktsioonidega kokku puutub.   
- **Süsteem** – saate ajutiselt keelata süsteemis olevad kõigi kasutajate kõik isikupärastamised. Sel juhul isikupärastamised kustutatakse. Kõik lehed lähtestatakse kõigi kasutajate puhul vaikeolekusse. Kui lubate isikupärastamise hiljem uuesti, rakendatakse kõik isikupärastamised uuesti. Saate ka kõigi kasutajate isikupärastamised süsteemist jäädavalt kustutada. Kustutatud isikupärastamisi ei ole võimalik taastada. Seega veenduge enne seda ülesannet, et oleksite eksportinud kõik isikupärastamised, mida võite soovida hiljem importida.

## <a name="personalization-of-inventory-dimensions"></a>Varude dimensioonide isikupärastamine.

Lehel varude dimensioonide häälestuse isikupärastamisel võtke arvesse suvandi **Kuva dimensiooni** abil loodud sätteid. Näiteks saate isikupärastamise abil peita partiinumbri varude dimensiooni veeru, kuid veerg kuvatakse järgmine kord, kui leht avatakse. Selle põhjuseks on asjaolu, et suvandi **Dimensiooni kuvamine** sätted juhivad kuvatavaid varude dimensiooni veerge.

**Dimensiooni kuva** sätted rakenduvad kõigil lehtedel ja alistavad igal eraldi lehel varude dimensiooniväljade isikupärastatud sätted.

Seega kui te eeltoodud näites ei soovi partiinumbri varude dimensiooni veergu lehel kuvada, peate selle dimensiooni selle lehe suvandi **Kuva dimensioonid** osana eemaldama.
