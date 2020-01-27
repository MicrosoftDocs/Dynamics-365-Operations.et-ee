---
title: Kasutuskogemuse isikupärastamine
description: Selles teemas selgitatakse, kuidas isikupärastada rakendust.
author: jasongre
manager: AnnBe
ms.date: 01/07/2020
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
ms.openlocfilehash: ac8f154fdf892553f69d135727589bf13efd6076
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935461"
---
# <a name="personalize-the-user-experience"></a>Kasutuskogemuse isikupärastamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas isikupärastada rakendust.

Isikupärastamise põhiklasse on kolm.

- Seadistuslehel tehtavad isikupärastamised. Näiteks võib tuua värvikujunduse ja ajavööndi.
- Lehe kasutusega seotud isikupärastamised. Neid isikupärastamisi teatakse *varjatud* isikupärastamisena. Näiteks jälgib süsteem ruudustiku veerulaiusi, kui neid korrigeerite, ja kiirkaartide laiendatud või ahendatud olekut.
- Isikupärastamised, mille kasutaja teeb lehe välimuse muutmiseks, muutes elemendi lehel ilmumise või toimimise viisi, sageli interaktiivse isikupärastamisrežiimi kaudu. Neid isikupärastamisi teatakse *otsese* isikupärastamisena. Näiteks võib kasutaja lehele elemente lisada, neid peita või ümber korraldada.

Kõik isikupärastamised, mille kasutaja teeb, on ainult sellele kasutajale olenemata isikupärastamise tüübist või ettevõttest, millega kasutaja parajasti suhtleb. Ühe kasutaja lehele tehtud muudatused ei mõjuta süsteemi teisi kasutajaid.

## <a name="system-wide-options-for-the-current-user"></a>Süsteemiülesed suvandid praegusele kasutajale

Leht **Kasutaja suvandid** sisaldab mitut süsteemiülest sätet praegusele kasutajale. Lehe **Kasutaja suvandid** avamiseks valige navigeerimisribal nupp **Sätted** (hammasrattaikoon) ja siis valige **Kasutaja suvandid**. Lehel **Kasutaja suvandid** on neli vahekaarti erinevate kasutajasätetega.

- **Visuaalne** – saate valida lehtede värvikujunduse ja elementide vaikesuurused.
- **Eelistused** – saate valida vaikeväärtused, mida kasutatakse iga kord, kui süsteemi avate. Väärtused hõlmavad ettevõtet, avalehte ja kuvamise/redigeerimise vaikerežiimi. (Kuva-/redigeerimisrežiim määrab, kas leht on vaatamiseks lukus või avaneb iga kord redigeerimiseks, kui selle avate.) Sellel vahekaardil on ka suvandid keele, ajavööndi ning kuupäeva-, kellaaja- ja numbrivormingute valimiseks. Samuti sisaldab see vahekaart mitmesuguseid eelistusi, mis erinevad olenevalt väljaandest.
- **Konto** – saate kohandada oma kasutajanime ja muid kontoga seotud suvandeid.
- **Töövoog** – saate valida seotud suvandeid.

Lisaks kasutajasätete muutmisele saate kasutusandmete ja isikupärastamiste vaatamiseks ja kustutamiseks lehte **Kasutaja valikud**. Valige vaid tegumiribal **Kasutusandmed**.

Rakenduse kasutamisel salvestatakse paljud teie valikud, et muuta süsteemi kasutamine tulevikus teie jaoks lihtsamaks. Süsteemi lehtedel tehtud isiklikke muudatusi võimaldab teil vaadata ja hallata vahekaart **Isikupärastamine**. Sellel vahekaardil saate lähtestada ka funktsiooni viiktekstid (st hüpikaknad, mis tutvustavad uusi süsteemifunktsioone). Seejärel teavitatakse teid uuesti eelnevatest funktsioonidest.

> [!NOTE]
> Kui funktsioon [Salvestatud vaated](saved-views.md) on sisse lülitatud, saate isikupärastamisi vaadata ja hallata, kui valite lehe **Kasutaja valikud** tegumiribal **Isikupärastamine**.

## <a name="implicit-personalizations"></a>Varjatud isikupärastamised

Varjatud isikupärastamised on need isikupärastamised, mida teete teatud juhtnuppe reguleerides, mis salvestavad praeguse nähtava oleku.

- **Ruudustiku veerud** – saate korrigeerida veeru laiust ruudustikus, valides veerupäisest vasakul või paremal oleva suuruse muutise riba ja libistades seda vasakule või paremale, kuni veerg on soovitud laiusega. Rakendus salvestab veeru jaoks valitud laiuse. Seejärel muudab see veeru laiuse valitud sättele järgmine kord, kui avate lehe, mis seda tabelit sisaldab.
- **Kiirkaardid** – mõnel lehel on laiendatavad jaotised, mida nimetatakse *kiirkaartideks*. Rakendus salvestab kiirkaartide laiendamise ja ahendamise teabe. Seejärel laiendatakse või ahendatakse samad kiirkaardid iga kord, kui lehe avate, võttes aluseks teie viimase tegevuse lehel. Mõnel juhul saate kiirkaardi ahendamisega aidata süsteemi jõudlust parandada, sest rakendus ei pea kiirkaartide teavet tooma, kuni neid ei laiendata. Nagu hiljem selles teemas on selgitatud, saate muuta ka kiirkaartide järjestust lehel.
- **Kiirinfo** – mõnedel lehtedel on paan **Seotud teave**, millel kuvatakse lehe praeguse teemaga seotud kirjutuskaitstud teave. Igat paani **Seotud teave** jaotist nimetatakse *Kiirinfoks*. Saate kogu paani **Seotud teave** peita või kuvada, samuti laiendada või ahendada üksikuid kiirinfosid. Rakendus salvestab need eelistused. Teie viimast tegevust lehel arvesse võttes laiendatakse või ahendatakse paani **Seotud teave** ja üksikuid kiirinfosid järgmine kord, kui lehe avate. Mõnel juhul saate kiirinfo ahendamisega aidata süsteemi jõudlust parandada, sest rakendus ei pea kiirinfo teavet tooma, kuni neid ei laiendata.
- **Toimingupaanid** – *toimingupaan* kuvatakse enamiku lehtede ülaserva lähedal. Toimingupaan sisaldab nuppe paljudeks tegevusteks, mida praegusel lehel saate teha. Need nupud on sageli korraldatud vahekaartidele. Saate kogu tegumiriba kinnitada avatuna või hoida selle vaikimisi ahendatuna. Seejärel avatakse või ahendatakse tegumiriba iga kord, kui lehe avate, võttes aluseks teie viimase tegevuse lehel. Kui olete tegumiriba kinnitanud, kuvatakse viimati kasutatud vahekaart.
- **Kiirfiltrid** – *kiirfilter* kuvatakse paljude ruudustike kohal. Kiirfiltriga saate ruudustikku filtreerida valitud veeru põhjal. Rakendus salvestab filtreeritud veeru valiku. Seejärel filtreeritakse ruudustik sama veeru järgi, kui seda ruudustikku sisaldava lehe järgmine kord avate. Siiski saate valida erineva veeru, mille alusel tabelit filtreerida.
- **Veerupäisefiltrid** – kui filtreerite ruudustiku *veerupäisefiltritega*, saate soovitud andmete leidmiseks muuta filtri operaatorit soovitud viisil. Näiteks saate valida tehtemärgi **algab väärtusega** asemel tehtemärgi **on täpselt**. Iga kord, kui kasutate veerupäisefiltrit ja muudate filtri tehtemärki, salvestab rakendus muudatuse. Seejärel taastab see filtri tehtemärgi järgmine kord, kui selle veeru alusel filtreerite.
- **Navigeerimispaan** – saate avada *navigeerimispaani*, valides mistahes lehe vasakul paanil nupu **Laienda navigeerimispaani**. (_**Menüü** nuppu_, nimetatakse mõnikord *hamburgeriks*, *hamburgerimenüük*s või *hamburgerinupuks*.) Saate kinnitada navigeerimispaani avatuna või hoida selle vaikimisi ahendatuna. Kui olete navigeerimispaani avatuna kinnitanud, hoiab rakendus seda lahti, kuni selle ahendate.

## <a name="explicit-personalizations"></a>Selged isikupärastamised

Erinevad inimesed ja ettevõtted näevad erineval moel andmeid, mis on nende jaoks olulisimad ja mis ei käitu viisil, nagu neil oma äri käitamiseks on vaja. Saate kohandada oma teabe korralduse ja sellega suhtlemise viisi. Saate ka määrata, et osa teabest peab olema peidetud. Need võimalused on aluseks isiklikule ja tulemuslikule kogemusele ning on näited sõnaselgetest isikupärastamistest. Selged isikupärastamised on isikupärastamised, mille teete selge kavatsusega muuta elemendi või lehe välimust või käitumist muuta.

### <a name="shortcut-menu-options"></a>Otseteemenüü suvandid

Otseteemenüüd pakuvad mitut võimalust lehe selgeks muutmiseks, et see vastaks paremini teie enda või teie ettevõtte nõuetele. (Otseteemenüüd nimetatakse ka *paremklõpsuga avatavaks menüüks* või *kontekstimenüüks*.)

Mõned tüüpilisimad ja olulisimad muudatused, mille lehele saab teha, on saadaval otse, kasutades otseteemenüü suvandeid. Näiteks kui soovite alates platvormivärskendusest 17 lisada ruudustikku veerge või neid peita, lihtsalt paremklõpsake veerupäisel ja siis valige käsk **Lisa veerge** või **Peida see veerg**.

Peale selle on enamik selge isikupärastamise tüüpe saadaval, kui paremklõpsate elemendil ja valite käsu **Isikupärastamine**. (Arvestage sellega, et kõiki lehel olevaid elemente ei saa isikupärastada.) Kui valite selle isikupärastamise viisi, ilmub elemendi atribuudiaken.

![Elemendi atribuutide isikupärastamine](./media/personalization-element-properties.png)

Atribuudiakna kaudu on elemendi isikupärastamiseks järgmised võimalused.

- Elemendi sildi muutmine.
- Elemendi peitmine, nii et seda lehel ei kuvata. Väljal olevaid andmeid ei kustutata ega muudeta. Lihtsalt lehel ei kuvata enam teavet.
- Teabe lisamine kiirkaardi kokkuvõttejaotisse (kui element on kiirkaardil).
- Jätke väli vahele, et seda ei saaks kunagi fokusseerida, kui te tabuleerite läbi lehe.
- Saate väljal olevate andmete (mis tahes kirje puhul) redigeerimist takistada.

Atribuudiaken võib sisaldada ka muid isikupärastamisvõimalusi olenevalt elemendist. Näiteks paani atribuudiaken võib lubada teil ülendada selle paani armatuurlauaks ja armatuurlaua atribuudiaken võib lubada teil luua sellel armatuurlaual uue tööruumi.

### <a name="the-personalization-toolbar"></a>Isikupärastamise tööriistariba

Kui soovite teha lehele mitu muudatust või teete muudatusi, mis pole muude mehhanismide (nt elementide ümberjärjestamine) kaudu saadaval, saate kasutada tööriistariba **Isikupärastamine**. Tööriistariba **Isikupärastamine** avamiseks toimige järgmiselt.

- Avage elemendi atribuutide aknas **Isikupärasta seda vormi**.
- Valige mistahes lehe vahekaardi **Suvandid** jaotise **Isikupärastamine** tegumiribal **Isikupärasta seda lehte**.
- Valige navigeerimisribal nupp **Sätted** (hammasrattasümbol) ja valige **Isikupärasta**.

[![Isikupärastamise tööriistariba](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Lehel liikumine

Kui tööriistariba **Isikupärastamine** on avatud, on aluseks olev leht kirjutuskaitstud (teiste sõnadega, te ei saa andmeid redigeerida), kuid see on siiski interaktiivne. Täpsemalt saate laiendada või ahendada paani **Seostuv teave**, vahetada vahekaarte ja laiendada või ahendada jaotisi, nagu tavaliselt neid toiminguid lehel teete. Isikupärastamismuudatuse rakendamiseks ahendatavale jaotisele või vahekaardile (nt kiirkaardi peitmine), käivitate vaid ahendatava jaotise või vahekaardi kõrval kuvatava nupu, kui sellele klaviatuuri või hiire abil liigute.

#### <a name="personalization-tools"></a>Isikupärastamise tööriistad

Tööriistaribal **Isikupärastamine** on saadaval järgmised tööriistad.

- Tööriistaga **Vali** saate valida ja muuta elemendi atribuute. Selle tööriista kasutamiseks valige tööriistaribal nupp **Vali** ja seejärel valige soovitud element. Kuvatakse elemendi atribuudiaken ja te saate muuta selle elemendi mistahes atribuute. Saate protsessi selle lehe muude isikupärastatavate elementide puhul korrata. Võtke arvesse, et mõned isikupärastamise atribuudid ei pruugi mõne stsenaariumi puhul saadaval olla. Näiteks ei saa te nõutavat välja lukustada.
- Tööriistaga **Peida** saate elemendi lehel peita. Selle tööriista kasutamiseks valige tööriistaribal nupp **Peida** ja seejärel valige peidetav element. Tööriista **Peida** kasutamisel muudetakse kõik parasjagu peidetud elemendid nähtavaks, kuid need kuvatakse varjutatud konteineris. Elemendi saate nähtavaks muuta, kui valite selle. Selleks, et vaadata, milline leht välja näeb, kui elemendid on peidetud, aktiveerige muu isikupärastamistööriist.
- Välja lisamiseks lehele kasutage tööriista **Välja lisamine**. Selle tööriista kasutamisel saate lisada ainult välju, mis on osa lehekülje määratlusest. Teavet selle kohta, kuidas luua uusi välju, mis ei ole osa praeguse lehe määratlusest, vt jaotisest [Kohandatud väljade loomine ja nendega töötamine](user-defined-fields.md). Nupu **Lisa väli** valimisel tööriistaribal, peate esmalt valima rühma või ala, kuhu soovite välja lisada. Dialoogiboksis kuvatakse valitud rühma või alaga seotud väljade loend. Valige dialoogiboksis lisamiseks üks või mitu välja ja seejärel valige käsk **Sisesta**. Varem lisatud välja eemaldamiseks korrake protsessi, kuid tühjendage dialoogiboksis välja valik.
- Tööriistaga **Teisalda** saate nihutada elemendi praeguses elemendirühmas teise asukohta. Võtke arvesse, et elementi ei saa teisaldada emagrupist väljapoole. Selle tööriista kasutamiseks valige tööriistaribal nupp **Teisalda** ja seejärel valige teisaldatav element. Elemendi valimisel määratleb rakendus asukohad, kuhu elementi saab teisaldada. Neid asukohti tuntakse *pukseerimistsoonidena*. Elemendi lohistamisel praeguses rühmas kuvatakse iga pukseerimistsoon värvilisena ja paksu joonega selle ala kõrval, kuhu elemendi saab pukseerida.
- Tööriistaga **Jäta vahele** saate eemaldada elemendi lehe klaviatuuri vahekaardijärjestusest. Nupu **Jäta vahele** valimisel tööriistaribal kuvatakse kõik parasjagu vahelejäetud elemendid varjutatud konteineris. Välju saate interaktiivselt vahekaardi järjestusest eemaldada või neid sinna lisada.
- Tööriistaga **Kuva päis** saate kuvada välja kiirkaardi kokkuvõttejaotises. Tööriistariba nupu **Kuva päises** valimisel kuvatakse kõik kokkuvõtteväljadena valitud väljad varjutatud konteineris. Saate välju interaktiivselt kiirkaardi kokkuvõttesse lisada ja neid sealt eemaldada, valides soovitud väljad.
- Tööriistaga **Lukusta** saate märkida elemendi redigeeritavaks või mitteredigeeritavaks. Nupu **Lukusta** valimisel tööriistaribal kuvatakse kõik parasjagu mitteredigeeritavad elemendid varjutatud konteineris. Seejärel saate need uuesti redigeeritavaks muuta. Arvestage sellega, et mõned väljad on nõutavad ja neid ei saa mitteredigeeritavaks muuta. Nende väljade kõrval kuvatakse tabalukuikoon.
- Kasutage nuppu **Lisa PowerApp** iga loodud rakenduse manustamiseks lehele rakendusega Microsoft PowerApps. Üksikasjalikku teavet lehele PowerAppsi rakenduse manustamise kohta vt jaotisest [PowerAppsi rakenduste manustamine](embed-power-apps.md).
- Kasutage tööriista **Eemaldamine** lehe lähtestamiseks vaikesätetele, installitud olekusse. Kõik praeguse lehe isikupärastamised kustutatakse. Tagasivõtmine ei ole võimalik. Seetõttu kasutage seda tööriista ainult siis, kui soovite lehe lähtestada.
- Tööriistaga **Importimine** saate laadida isikupärastamise failist, mille teie või keegi teine on lehe jaoks varem loonud. Kui impordite lehele isikupärastamised, saate valida, kas need tuleks lisada lehele või asendada kõik teie olemasolevad isikupärastamised. Tagasivõtmine ei ole võimalik. Seetõttu peate pärast isikupärastamise importimist käsitsi eemaldama või tühistama kõik soovitud muudatused.
- Tööriistaga **Eksportimine** saate oma lehe isikupärastamised failina salvestada. Saate seejärel oma isikupärastamisi teiste kasutajatega jagada. Need kasutajad peavad lihtsalt importima teie lehe isikupärastamisi sisaldava faili.
- Valige nupp **Sule**, kui soovite tööriistariba **Isikupärastamine** sulgeda ja lehe eelmise interaktiivse oleku taastada.

Traditsiooniliselt, kui kasutate tööriistariba **Isikupärastamine**, jõustuvad teie isikupärastamised kohe, kui need teete. Kui aga funktsioon [Salvestatud vaated](saved-views.md) on sisse lülitatud, peate isikupärastamised kindlasti salvestama valitud vaatesse.

Mõnel juhul kuvatakse tööriista valimisel elemendi kõrval tabalukuikoon. See ikoon näitab, et valitud tööriistaga seotud elemendi atribuute ei saa muuta, kuna nende atribuutide muutmine takistab lehe korralikku toimimist.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Tööruumile paani, loendi või lingi lisamine

Mõned lehed, milles on loendid, on isikupärastamisfunktsioon **Lisa tööruumi** saadaval tegumiriba vahekaardi **Suvandid** jaotises **Isikupärastamine**. Selle funktsiooni abil saate praegusest loendist lükata vastava teabe kindlasse tööruumi. Tööruumis kuvatav teave võib põhineda kas tervel loendil või loendi filtreeritud ja sorditud versioonis. Samuti saate määrata, kas teave kuvatakse tööruumis loendina, kokkuvõttepaanina, mis võib näidata loendis olevate üksuste arvu, või lingina.

> [!NOTE]
> Kui funktsioon [Salvestatud vaated](saved-views.md) on sisse lülitatud, on tööruumi lükatud sisu vaatega otse lingitud. Vaate päringut kasutatakse tööruumis olevate andmete toomiseks ja tööruumi vastav paan või link avab selle vaate lehe, nii et selle jaoks rakendatakse vaate päring ja isikupärastamised.

[![Lisa tööruumi](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Tööruumile loendi lisamiseks tööruumi sortige või filtreerige esmalt lehel loend, et see kuvaks teavet nii, nagu soovite seda tööruumis kuvada. (Kui funktsioon Salvestatud vaated on sisse lülitatud, ei saa te jätkata enne, kui salvestate nende tingimustega vaate.) Seejärel valige **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Loend**. Pärast suvandi **Konfigureeri** valimist ilmub dialoogiboks, kus saate valida veerud, mis peaks tööruumis loendis ilmuma. Saate ka määrata tööruumis olevale loendile sildi.
- Tööruumile paani lisamiseks filtreerige esmalt lehel loendit, et see kuvaks andmed, mida tuleks kokku võtta või millele soovite kiiret juurdepääsu. (Kui funktsioon Salvestatud vaated on sisse lülitatud, ei saa te jätkata enne, kui salvestate nende tingimustega vaate.) Seejärel valige **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Paan**. Kui olete valinud suvandi **Konfigureeri**, ilmub dialoogiboks, kus saate määrata tööruumis olevale paanile sildi. Saate ka määrata, kas paanil kuvatakse arv. Pärast seda, kui paan on tööruumi lisatud, saate selle valida praeguse lehe avamiseks tööruumist. Seejärel saate vaadata paaniga seotud filtreeritud loendit.
- Tööruumile lingi lisamiseks filtreerige esmalt lehel loend, nii et see kuvaks andmeid, millest olete huvitatud. (Kui funktsioon Salvestatud vaated on sisse lülitatud, ei saa te jätkata enne, kui salvestate nende tingimustega vaate.) Seejärel valige **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Link**. Kui olete valinud suvandi **Konfigureeri**, ilmub dialoogiboks, kus saate määrata tööruumis olevale lingile sildi. Samuti saate valikuliselt määrata sildi uuele jaotisele, mis seda linki sisaldab.

Kui loend, paan või link on tööruumile lisatud, saate selle tööruumi avada ja elemendid soovitud viisil ümberkorraldada.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Kokkuvõtte lisamine tööruumist armatuurlauale

Mõni tööruum sisaldab arvpaane (st paane, millel on arvud) ja teil on võimalik ka need paanid armatuurlaual kuvada. Tööruumis paremklõpsake inventuuripaani, valige **Isikupärasta** ja seejärel valige paani atribuutide aknas **Kinnita armatuurlauale**. Järgmine kord, kui te valitud armatuurlaua avate ja värskendate, kuvatakse arv selle tööruumi navigeerimispaani all. Saate suunata selle arvu otse asjassepuutuvate andmete juurde.

### <a name="personalizing-your-dashboard"></a>Armatuurlaua isikupärastamine

Armatuurlaud on tihti esimene leht, mida näete rakenduse avamisel. Saate armatuurlaua isikupärastada, nii et sellel kuvatakse ainult need tööruumi paanid, mida soovite näha. Saate paane ka ümber korraldada nii, et need kuvatakse soovitud järjestuses, tööruumi navigeerimispaanid ümber nimetada või lisada uue tööruumipaani.

Armatuurlaua isikupärastamiseks lihtsalt paremklõpsake mis tahes paanil ja valige suvand **Isikupärastamine**, et avada paani atribuudiaken.

- Kui soovite valitud paani peita või ümber nimetada, saate muudatuse teha otse atribuudiaknas.
- Tööruumi paanide ümberjärjestamiseks valige atribuudiaknas suvand **Selle vormi isikupärastamine**, et avada tööriistariba **Isikupärastamine**. Seejärel saate kasutada paanide soovitud viisil ümberkorraldamiseks tööriista **Teisalda**.
- Uue tööruumipaani lisamiseks valige atribuudiaknas käsk **Lisa tööruum**. Uus tööruumipaan luuakse armatuurlaua alaserva. Saate selle uue tööruumipaani soovitud viisil ümber nimetada. Samuti lisada tööruumi loendeid, paane ja linke, nagu on kirjeldatud selle teema jaotises [Tööruumidesse loendite, paanide või linkide lisamine](#adding-a-tile-list-or-link-to-a-workspace).

## <a name="administration-of-personalizations"></a>Isikupärastamiste haldamine

Pärast lehe isikupärastamist võite oma isikupärastamisi oma isikupärastatud lehe eksportimise teel teiste kasutajatega jagada. Seejärel võite paluda teistel kasutajatel avada isikupärastatud leht ja importida teie loodud isikupärastamise fail. Teine võimalus on anda oma isikupärastamised administraatoriõigustega kasutajale. See kasutaja saab seejärel rakendada teie isikupärastamisfaili korraga paljudele kasutajatele.

Administraatori õigustega kasutaja saab lehel **Isikupärastamine** hallata ka teiste kasutajate isikupärastamisi.

Klientidele, kes pole funktsiooni [Salvestatud vaated](saved-views.md) sisse lülitanud, on sellel lehel neli vahekaarti.

- **Rakenda** – saate importida või valida vähemalt ühe kasutaja isikupärastamise. Isikupärastamise rakendamiseks ühele või mitmele kasutajale valige esmalt roll ja selle rolliga kasutajad. Seejärel valige kas olemasolev isikupärastamine valitud kasutajatele rakendamiseks või importige isikupärastamise fail. Isikupärastamine kinnitatakse ja rakendatakse valitud kasutajatele järgmisel korral, kui nad valitud lehe avavad.
- **Eemalda** – saate eemaldada vähemalt ühe kasutaja lehe või tööruumi kõik isikupärastamised. Esmalt valige leht või tööruum, et näha seda isikupärastanud kasutajate loendit. Seejärel valige kasutajad, kelle isikupärastamised tuleb sellelt lehelt või sellest tööruumist eemaldada, ja valige käsk **Eemalda**. Kõik isikupärastamised, mille valitud kasutajad on valitud lehele või tööruumile rakendanud, kustutatakse. Seda tegevust ei saa tagasi võtta. Kui aga isikupärastamine on lehele või tööruumile salvestatud, saab selle isikupärastamise uuesti importida.
- **Kasutajad** – saate valida kasutaja, et kuvada loend lehtedest, mille kasutaja on isikupärastanud. Seejärel saate valitud kasutaja võimaluse kasutada isikupärastamisi kindlatel lehtedel või terves süsteemis sisse või välja lülitada. Samuti saate kasutaja jaoks isikupärastamise importida, eksportida või eemaldada. Lisaks saate lähtestada kasutaja funktsiooni viiktekstid. Sel juhul, kui kasutaja on varem välja lülitanud kõik hüpikaknad, mis juurutavad uusi funktsioone, kuvatakse need uuesti järgmisel korral, kui kasutaja nende funktsioonidega kokku puutub.
- **Süsteem** – saate ajutiselt välja lülitada süsteemis olevad kõigi kasutajate kõik isikupärastamised. Sel juhul kustutatakse kõik isikupärastamised kõigi kasutajate jaoks ja kõik lehed lähtestatakse nende vaikeolekusse. Kui lülitate isikupärastamise hiljem uuesti sisse, rakendatakse kõik isikupärastamised uuesti. Saate ka kõigi kasutajate isikupärastamised süsteemist jäädavalt kustutada. Kustutatud isikupärastamisi ei ole võimalik taastada. Seega veenduge enne seda ülesannet, et oleksite eksportinud kõik isikupärastamised, mida võite soovida hiljem importida.

Klientidele, kes on funktsiooni [Salvestatud vaated](saved-views.md) sisse lülitanud, on lehel **Isikupärastamine** viis vahekaarti.

- **Avaldatud vaated** – need vaated on teie organisatsioonile avaldatud. Nende vaadete sihtrühmaks olevate kasutajate muutmiseks saate muuta iga vaatega seotud turberolli või juriidilisi isikuid. Saate eksportida või kustutada ka ühe või mitu avaldatud vaadet.
- **Avaldamata vaated** – need vaated on mallivaated, mis on imporditud teie süsteemi, kuid pole veel avaldatud. Saate neid vaateid avaldada, eksportida või kustutada.
- **Isiklikud vaated** – need vaated on loodud süsteemi kasutajate poolt. Saate avaldada organisatsioonile isikliku vaate või kopeerida ühe või mitu neist vaadetest teistele kasutajatele. Saate neid vaateid vajadusel ka eksportida või kustutada.
- **Kasutajad** – saate valida kasutaja, et kuvada loend lehtedest, mille kasutaja on isikupärastanud. Seejärel saate valitud kasutaja võimaluse kasutada isikupärastamisi kindlatel lehtedel või terves süsteemis sisse või välja lülitada. Samuti saate kasutaja jaoks isikupärastamise importida, eksportida või eemaldada. Lisaks saate lähtestada kasutaja funktsiooni viiktekstid. Sel juhul, kui kasutaja on varem välja lülitanud kõik hüpikaknad, mis juurutavad uusi funktsioone, kuvatakse need uuesti järgmisel korral, kui kasutaja nende funktsioonidega kokku puutub.
- **Süsteem** – saate ajutiselt välja lülitada süsteemis olevad kõigi kasutajate kõik isikupärastamised. Sel juhul kustutatakse kõik isikupärastamised kõigi kasutajate jaoks ja kõik lehed lähtestatakse nende vaikeolekusse. Kui lülitate isikupärastamise hiljem uuesti sisse, rakendatakse kõik isikupärastamised uuesti. Saate ka kõigi kasutajate isikupärastamised süsteemist jäädavalt kustutada. Kustutatud isikupärastamisi ei ole võimalik taastada. Seega veenduge enne seda ülesannet, et oleksite eksportinud kõik isikupärastamised, mida võite soovida hiljem importida.

Kasutajad, kellel on juurdepääs lehele **Isikupärastamine**, saavad tegumiriba nupu **Impordi vaated** abil ka isiklikke ja mallivaateid importida.

## <a name="personalizing-inventory-dimensions"></a>Varude dimensioonide isikupärastamine

Lehel varude dimensioonide häälestuse isikupärastamisel võtke arvesse suvandi **Kuva dimensiooni** abil loodud sätteid. Näiteks saate isikupärastamise abil peita partiinumbri varude dimensiooni veeru, kuid veerg kuvatakse järgmine kord, kui leht avatakse. Selle põhjuseks on asjaolu, et suvandi **Dimensiooni kuvamine** sätted juhivad kuvatavaid varude dimensiooni veerge. **Dimensiooni kuva** sätted rakenduvad kõigile lehtede ja alistavad eraldi lehtedel varude dimensiooniväljade isikupärastatud sätted.

Seega, kui te eeltoodud näites ei soovi partiinumbri varude dimensiooni veergu lehel kuvada, peate selle dimensiooni selle lehe suvandi **Kuva dimensioonid** osana eemaldama.
